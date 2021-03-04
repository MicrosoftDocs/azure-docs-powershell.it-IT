---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 87a50c69449437401ff26b76b87cf0f334ab8d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975886"
---
# <span data-ttu-id="59aeb-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="59aeb-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="59aeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="59aeb-103">Rimuove un servizio collegato da Data factory.</span><span class="sxs-lookup"><span data-stu-id="59aeb-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="59aeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59aeb-104">SYNTAX</span></span>

### <span data-ttu-id="59aeb-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="59aeb-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59aeb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59aeb-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59aeb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59aeb-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59aeb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59aeb-108">DESCRIPTION</span></span>
<span data-ttu-id="59aeb-109">Il cmdlet Remove-AzDataFactoryV2LinkedService rimuove un servizio collegato da Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="59aeb-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="59aeb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59aeb-110">EXAMPLES</span></span>

### <span data-ttu-id="59aeb-111">Esempio 1: Rimuovere un servizio collegato</span><span class="sxs-lookup"><span data-stu-id="59aeb-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="59aeb-112">Questo comando rimuove il servizio collegato denominato LinkedServiceTest dal data factory denominato WikiADF.</span><span class="sxs-lookup"><span data-stu-id="59aeb-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="59aeb-113">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="59aeb-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="59aeb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59aeb-114">PARAMETERS</span></span>

### <span data-ttu-id="59aeb-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="59aeb-115">-DataFactoryName</span></span>
<span data-ttu-id="59aeb-116">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="59aeb-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="59aeb-117">Questo cmdlet rimuove un servizio collegato dal data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="59aeb-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59aeb-118">-DefaultProfile</span></span>
<span data-ttu-id="59aeb-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59aeb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-120">-Force</span><span class="sxs-lookup"><span data-stu-id="59aeb-120">-Force</span></span>
<span data-ttu-id="59aeb-121">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="59aeb-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59aeb-122">-InputObject</span></span>
<span data-ttu-id="59aeb-123">Specifica l'oggetto LinkedService da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="59aeb-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="59aeb-124">-Name</span></span>
<span data-ttu-id="59aeb-125">Specifica il nome del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="59aeb-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="59aeb-126">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="59aeb-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59aeb-127">-ResourceGroupName</span></span>
<span data-ttu-id="59aeb-128">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="59aeb-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="59aeb-129">Questo cmdlet rimuove un servizio collegato dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="59aeb-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59aeb-130">-ResourceId</span></span>
<span data-ttu-id="59aeb-131">ID della risorsa Azure del servizio collegato da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="59aeb-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59aeb-132">-Confirm</span></span>
<span data-ttu-id="59aeb-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59aeb-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59aeb-134">-WhatIf</span></span>
<span data-ttu-id="59aeb-135">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="59aeb-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59aeb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59aeb-136">CommonParameters</span></span>
<span data-ttu-id="59aeb-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59aeb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59aeb-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59aeb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59aeb-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="59aeb-139">INPUTS</span></span>

### <span data-ttu-id="59aeb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="59aeb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="59aeb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="59aeb-141">System.String</span></span>

## <span data-ttu-id="59aeb-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59aeb-142">OUTPUTS</span></span>

### <span data-ttu-id="59aeb-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="59aeb-143">System.Void</span></span>

## <span data-ttu-id="59aeb-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="59aeb-144">NOTES</span></span>
<span data-ttu-id="59aeb-145">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="59aeb-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="59aeb-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59aeb-146">RELATED LINKS</span></span>

[<span data-ttu-id="59aeb-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="59aeb-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="59aeb-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="59aeb-148">Set-AzDataFactoryV2LinkedService</span></span>]()

