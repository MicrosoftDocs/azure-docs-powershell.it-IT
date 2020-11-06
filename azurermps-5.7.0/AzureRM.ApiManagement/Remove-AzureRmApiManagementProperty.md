---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProperty.md
ms.openlocfilehash: d8c47cb6aaf1f135cd08110f4ab1d616cb105f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508431"
---
# <span data-ttu-id="c317d-101">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c317d-101">Remove-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="c317d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c317d-102">SYNOPSIS</span></span>
<span data-ttu-id="c317d-103">Rimuove una proprietà di gestione API.</span><span class="sxs-lookup"><span data-stu-id="c317d-103">Removes an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c317d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c317d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c317d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c317d-105">DESCRIPTION</span></span>
<span data-ttu-id="c317d-106">Il cmdlet **Remove-AzureRmApiManagementProperty** rimuove una **Proprietà** di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="c317d-106">The **Remove-AzureRmApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="c317d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c317d-107">EXAMPLES</span></span>

### <span data-ttu-id="c317d-108">Esempio 1: rimuovere una proprietà</span><span class="sxs-lookup"><span data-stu-id="c317d-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="c317d-109">Questo comando rimuove la proprietà con ID Property11.</span><span class="sxs-lookup"><span data-stu-id="c317d-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="c317d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c317d-110">PARAMETERS</span></span>

### <span data-ttu-id="c317d-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c317d-111">-Context</span></span>
<span data-ttu-id="c317d-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c317d-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c317d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c317d-113">-DefaultProfile</span></span>
<span data-ttu-id="c317d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c317d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c317d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c317d-115">-PassThru</span></span>
<span data-ttu-id="c317d-116">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c317d-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c317d-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="c317d-117">-PropertyId</span></span>
<span data-ttu-id="c317d-118">Specifica un ID della proprietà rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c317d-118">Specifies an ID of the property that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c317d-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c317d-119">-Confirm</span></span>
<span data-ttu-id="c317d-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c317d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c317d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c317d-121">-WhatIf</span></span>
<span data-ttu-id="c317d-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c317d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c317d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c317d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c317d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c317d-124">CommonParameters</span></span>
<span data-ttu-id="c317d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c317d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c317d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c317d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c317d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c317d-127">INPUTS</span></span>

### <span data-ttu-id="c317d-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c317d-128">None</span></span>
<span data-ttu-id="c317d-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c317d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c317d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c317d-130">OUTPUTS</span></span>

### <span data-ttu-id="c317d-131">bool</span><span class="sxs-lookup"><span data-stu-id="c317d-131">bool</span></span>

## <span data-ttu-id="c317d-132">Note</span><span class="sxs-lookup"><span data-stu-id="c317d-132">NOTES</span></span>

## <span data-ttu-id="c317d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c317d-133">RELATED LINKS</span></span>

[<span data-ttu-id="c317d-134">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c317d-134">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="c317d-135">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="c317d-135">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


