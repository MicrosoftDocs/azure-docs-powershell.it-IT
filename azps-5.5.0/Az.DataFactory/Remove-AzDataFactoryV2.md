---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180999"
---
# <span data-ttu-id="ff6c4-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff6c4-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="ff6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6c4-103">Rimuove un data factory.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-103">Removes a data factory.</span></span>

## <span data-ttu-id="ff6c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff6c4-104">SYNTAX</span></span>

### <span data-ttu-id="ff6c4-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="ff6c4-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6c4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ff6c4-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff6c4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ff6c4-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6c4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ff6c4-108">DESCRIPTION</span></span>
<span data-ttu-id="ff6c4-109">Il cmdlet Remove-AzDataFactoryV2 rimuove un data factory.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="ff6c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff6c4-110">EXAMPLES</span></span>

### <span data-ttu-id="ff6c4-111">Esempio 1: Rimuovere un data factory</span><span class="sxs-lookup"><span data-stu-id="ff6c4-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="ff6c4-112">Questo comando rimuove il data factory denominato WikiADF dal gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="ff6c4-113">Questo comando restituisce il valore $True.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ff6c4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff6c4-114">PARAMETERS</span></span>

### <span data-ttu-id="ff6c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6c4-115">-DefaultProfile</span></span>
<span data-ttu-id="ff6c4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff6c4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ff6c4-117">-Force</span></span>
<span data-ttu-id="ff6c4-118">Esegue il cmdlet senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ff6c4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff6c4-119">-InputObject</span></span>
<span data-ttu-id="ff6c4-120">Specifica l'oggetto DataFactory da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff6c4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ff6c4-121">-Name</span></span>
<span data-ttu-id="ff6c4-122">Specifica il nome del data factory da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff6c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff6c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="ff6c4-124">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ff6c4-125">Questo cmdlet rimuove un data factory dal gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff6c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff6c4-126">-ResourceId</span></span>
<span data-ttu-id="ff6c4-127">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ff6c4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff6c4-128">-Confirm</span></span>
<span data-ttu-id="ff6c4-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6c4-130">-WhatIf</span></span>
<span data-ttu-id="ff6c4-131">Mostra cosa succede se il cmdlet viene eseguito, ma non lo esegue.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ff6c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6c4-132">CommonParameters</span></span>
<span data-ttu-id="ff6c4-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6c4-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6c4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6c4-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ff6c4-135">INPUTS</span></span>

### <span data-ttu-id="ff6c4-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ff6c4-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="ff6c4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ff6c4-137">System.String</span></span>

## <span data-ttu-id="ff6c4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff6c4-138">OUTPUTS</span></span>

### <span data-ttu-id="ff6c4-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="ff6c4-139">System.Void</span></span>

## <span data-ttu-id="ff6c4-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ff6c4-140">NOTES</span></span>
<span data-ttu-id="ff6c4-141">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="ff6c4-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ff6c4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff6c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff6c4-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff6c4-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="ff6c4-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff6c4-144">Set-AzDataFactoryV2</span></span>]()
