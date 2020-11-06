---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: CD582654-1B0C-4960-9E18-454F857B56E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagement.md
ms.openlocfilehash: 197b1605d178c0aaa1c3f96580cb295306910232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521115"
---
# <span data-ttu-id="5560b-101">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560b-101">Remove-AzureRmApiManagement</span></span>

## <span data-ttu-id="5560b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5560b-102">SYNOPSIS</span></span>
<span data-ttu-id="5560b-103">Rimuove un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="5560b-103">Removes an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5560b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5560b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5560b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5560b-105">DESCRIPTION</span></span>
<span data-ttu-id="5560b-106">Il cmdlet **Remove-AzureRmApiManagement** rimuove un servizio di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="5560b-106">The **Remove-AzureRmApiManagement** cmdlet removes an Azure API Management service.</span></span>

## <span data-ttu-id="5560b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5560b-107">EXAMPLES</span></span>

### <span data-ttu-id="5560b-108">Esempio 1: rimuovere un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="5560b-108">Example 1: Remove an API Management service</span></span>
```
PS C:\>Remove-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi"
```

<span data-ttu-id="5560b-109">Questo comando rimuove il servizio di gestione delle API denominato ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="5560b-109">This command removes the API Management service named ContosoApi.</span></span>

## <span data-ttu-id="5560b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5560b-110">PARAMETERS</span></span>

### <span data-ttu-id="5560b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5560b-111">-DefaultProfile</span></span>
<span data-ttu-id="5560b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5560b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5560b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5560b-113">-Name</span></span>
<span data-ttu-id="5560b-114">Specifica il nome della distribuzione di gestione delle API rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5560b-114">Specifies the name of the API Management deployment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5560b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5560b-115">-PassThru</span></span>
<span data-ttu-id="5560b-116">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="5560b-116">Indicates that this cmdlet returns a value of $True if the operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5560b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5560b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5560b-118">Specifica il nome del gruppo di risorse in cui è presente la distribuzione di gestione API.</span><span class="sxs-lookup"><span data-stu-id="5560b-118">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="5560b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5560b-119">-Confirm</span></span>
<span data-ttu-id="5560b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5560b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5560b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5560b-121">-WhatIf</span></span>
<span data-ttu-id="5560b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5560b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5560b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5560b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5560b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5560b-124">CommonParameters</span></span>
<span data-ttu-id="5560b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5560b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5560b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5560b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5560b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5560b-127">INPUTS</span></span>

### <span data-ttu-id="5560b-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5560b-128">None</span></span>
<span data-ttu-id="5560b-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5560b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5560b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5560b-130">OUTPUTS</span></span>

### <span data-ttu-id="5560b-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5560b-131">System.Boolean</span></span>

## <span data-ttu-id="5560b-132">Note</span><span class="sxs-lookup"><span data-stu-id="5560b-132">NOTES</span></span>

## <span data-ttu-id="5560b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5560b-133">RELATED LINKS</span></span>

[<span data-ttu-id="5560b-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560b-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="5560b-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560b-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="5560b-136">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560b-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="5560b-137">Ripristinare-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5560b-137">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


