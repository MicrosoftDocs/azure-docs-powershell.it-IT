---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188892"
---
# <span data-ttu-id="8b6d2-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="8b6d2-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="8b6d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6d2-103">Salva il log di un'esecuzione di script di distribuzione su disco.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="8b6d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b6d2-104">SYNTAX</span></span>

### <span data-ttu-id="8b6d2-105">SaveDeploymentScriptLogByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b6d2-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b6d2-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b6d2-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6d2-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b6d2-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b6d2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b6d2-108">DESCRIPTION</span></span>
<span data-ttu-id="8b6d2-109">**Salva-AzDeploymentScriptLog** Salva il log di un'esecuzione di script di distribuzione su disco.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="8b6d2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b6d2-110">EXAMPLES</span></span>

### <span data-ttu-id="8b6d2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b6d2-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="8b6d2-112">Salva il log di uno script di distribuzione con il nome e il gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="8b6d2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b6d2-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="8b6d2-114">Salva le ultime 3 righe del log di uno script di distribuzione con il nome e il gruppo di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="8b6d2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b6d2-115">PARAMETERS</span></span>

### <span data-ttu-id="8b6d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6d2-116">-DefaultProfile</span></span>
<span data-ttu-id="8b6d2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b6d2-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="8b6d2-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="8b6d2-119">Oggetto PowerShell per lo script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6d2-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="8b6d2-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="8b6d2-121">ID risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="8b6d2-122">Esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="8b6d2-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6d2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8b6d2-123">-Force</span></span>
<span data-ttu-id="8b6d2-124">Impone la sovrascrittura del file esistente.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="8b6d2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b6d2-125">-Name</span></span>
<span data-ttu-id="8b6d2-126">Nome dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6d2-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="8b6d2-127">-OutputPath</span></span>
<span data-ttu-id="8b6d2-128">Percorso della directory in cui salvare il log degli script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6d2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6d2-129">-ResourceGroupName</span></span>
<span data-ttu-id="8b6d2-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6d2-131">-Coda</span><span class="sxs-lookup"><span data-stu-id="8b6d2-131">-Tail</span></span>
<span data-ttu-id="8b6d2-132">Limitare l'output all'ultima n righe</span><span class="sxs-lookup"><span data-stu-id="8b6d2-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6d2-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b6d2-133">-Confirm</span></span>
<span data-ttu-id="8b6d2-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b6d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b6d2-135">-WhatIf</span></span>
<span data-ttu-id="8b6d2-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6d2-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b6d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6d2-138">CommonParameters</span></span>
<span data-ttu-id="8b6d2-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b6d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6d2-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b6d2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6d2-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b6d2-141">INPUTS</span></span>

### <span data-ttu-id="8b6d2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8b6d2-142">System.String</span></span>

## <span data-ttu-id="8b6d2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b6d2-143">OUTPUTS</span></span>

### <span data-ttu-id="8b6d2-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="8b6d2-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="8b6d2-145">Note</span><span class="sxs-lookup"><span data-stu-id="8b6d2-145">NOTES</span></span>

## <span data-ttu-id="8b6d2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b6d2-146">RELATED LINKS</span></span>
