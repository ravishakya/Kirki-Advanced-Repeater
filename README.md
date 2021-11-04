# Kirki Advanced Repeater

**Author      :** Ravi Shakya  
**Author URI  :** https://bizbergthemes.com  
**License     :** GNU General Public License v2 or later  
**License URI :** http://www.gnu.org/licenses/gpl-2.0.html  
**Version     :** 0.1

## Description ##

Create repeaters with more controls

![ScreenRecorderProject2](https://user-images.githubusercontent.com/11089018/140257501-b3937dc8-594d-47e3-b692-e2ab78a4e079.gif)

## Example Code ##

````php
Kirki::add_field( 'bizberg', array(
    'type'        => 'advanced-repeater',
    'label'       => 'Repeater',
    'section'     => 'detail_page',
    'settings'    => 'advanced-repeater',
    'description' => 'Advanced Repeater',
    'default'      => json_encode([
        [
            'custom_fields' => 'textarea',
            'text_field'  => 'How are you',
            'content'=> 'This is an advanced repeater',
            'color_field' => '#000',
        ],
        [
            'custom_fields' => 'radio',
            'text_field'  => 'Good Morning',
            'content'=> 'Have a good day',
            'color_field'      => '#fff',
        ]
    ]),
    'choices' => [
        'limit' => 3,
        'button_label' => 'Add row',
        'row_label' => [
            'value' => 'Repeater',
        ],
        'fields' => [
            'custom_fields'  => [
                'type'        => 'select',
                'label'       => 'Custom Fields',
                'default'     => 'text',
                'choices'     => [
                    'text'        => 'Text',
                    'textarea'    => 'Textarea',
                    'color'       => 'Color',
                    'select'      => 'Select',
                    'image'       => 'Image',
                    'checkbox'    => 'Checkbox',
                    'radio'       => 'Radio',
                    'fontawesome' => 'Fontawesome',
                    'number'      => 'Number',
                    'date'        => 'Date'
                ],
            ],
            'color_option1' => [
                'type'        => 'heading',
                'label'       => 'Text Field',
                'choices'     => [
                    'background'  => '#ff5722'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'text'
                    ]
                ],
            ],
            'text_field' => [
                'type'        => 'text',
                'label'       => 'Text Field',
                'default'     => 'This is a text field',
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'text'
                    ]
                ],
            ],
            'color_option2' => [
                'type'        => 'heading',
                'label'       => 'Textarea Field',
                'choices'     => [
                    'background'  => '#607d8b'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'textarea'
                    ]
                ],
            ],
            'content'  => [
                'type'        => 'textarea',
                'label'       => 'Description',
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'textarea'
                    ]
                ],
            ],
            'color_option3' => [
                'type'        => 'heading',
                'label'       => 'Color Field',
                'choices'     => [
                    'background'  => '#9e9e9e'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'color'
                    ]
                ],
            ],
            'color_field'  => [
                'type'        => 'color',
                'label'       => 'Icon Color',
                'default'     => '#dd3333',
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'color'
                    ]
                ],
            ],	
            'color_option4' => [
                'type'        => 'heading',
                'label'       => 'Select Field',
                'choices'     => [
                    'background'  => '#795548'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'select'
                    ]
                ],
            ],
            'select_field'  => [
                'type'        => 'select',
                'label'       => 'Select Field',
                'choices'     => [
                    'text'     => 'Text',
                    'textarea' => 'Textarea',
                    'color'    => 'Color',
                    'select'   => 'Select',
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'select'
                    ]
                ],
            ],
            'image_field' => [
                'type'        => 'heading',
                'label'       => 'Image Field',
                'choices'     => [
                    'background'  => '#ff5722'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'image'
                    ]
                ],
            ],
            'slider_image'  => [
                'type'        => 'image',
                'label'       => 'Slider Image',
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'image'
                    ]
                ],
            ],	
            'checkbox_field' => [
                'type'        => 'heading',
                'label'       => 'Checkbox',
                'choices'     => [
                    'background'  => '#ff9800'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'checkbox'
                    ]
                ],
            ],
            'slider_status'  => [
                'type'        => 'checkbox',
                'label'       => 'Slider',
                'default'     => false,
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'checkbox'
                    ]
                ],
            ],
            'radio_field' => [
                'type'        => 'heading',
                'label'       => 'Radio',
                'choices'     => [
                    'background'  => '#cddc39'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'radio'
                    ]
                ],
            ],
            'laptops'  => [
                'type'        => 'radio',
                'label'       => 'Laptops',
                'choices'     => [
                    'dell'     => 'Dell',
                    'acer'     => 'Acer',
                    'samsung'  => 'Samsung'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'radio'
                    ]
                ],					
            ],	
            'fontawesome_field' => [
                'type'        => 'heading',
                'label'       => 'Fontawesome',
                'choices'     => [
                    'background'  => '#009688'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'fontawesome'
                    ]
                ],
            ],
            'icon'  => [
                'type'        => 'fontawesome',
                'label'       => 'Icon',
                'description' => 'Fontawesome Icons',
                'default'     => 'fab fa-accusoft',
                'choices'     => [
                    'fab fa-500px'           => '500',
                    'fab fa-accessible-icon' => 'Accessible Icon',
                    'fab fa-accusoft'        => 'Accusoft',
                    'fab fa-apper'           => 'Apper'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'fontawesome'
                    ]
                ],
            ],	
            'number_field' => [
                'type'        => 'heading',
                'label'       => 'Number',
                'choices'     => [
                    'background'  => '#3f51b5'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'number'
                    ]
                ],
            ],		
            'age' => [
                'type'        => 'number',
                'label'       => 'Age',
                'default'     => 30,
                'choices'     => [
                    'min'  => -10,
                    'max'  => 80,
                    'step' => 10,
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'number'
                    ]
                ],
            ],	
            'date_field' => [
                'type'        => 'heading',
                'label'       => 'Number',
                'choices'     => [
                    'background'  => 'purple'
                ],
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'date'
                    ]
                ],
            ],
            'datep'  => [
                'type'        => 'date',
                'label'       => 'Custom Fields',
                'description' => 'This is date control',
                'default'     => '2020-09-09',
                'active_callback' => [
                    [
                        'setting'  => 'custom_fields',
                        'operator' => '==',
                        'value'    => 'date'
                    ]
                ],
            ],		
        ]
    ]
) );
````
