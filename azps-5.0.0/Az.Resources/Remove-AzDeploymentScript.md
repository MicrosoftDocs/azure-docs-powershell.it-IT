---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203304"
---
# <span data-ttu-id="55b7e-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="55b7e-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="55b7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="55b7e-103">Rimuove uno script di distribuzione e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="55b7e-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="55b7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55b7e-104">SYNTAX</span></span>

### <span data-ttu-id="55b7e-105">RemoveDeploymentScriptLogByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55b7e-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55b7e-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="55b7e-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55b7e-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="55b7e-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b7e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55b7e-108">DESCRIPTION</span></span>
<span data-ttu-id="55b7e-109">Il cmdlet **Remove-AzDeploymentScript** rimuove uno script di distribuzione e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="55b7e-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="55b7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55b7e-110">EXAMPLES</span></span>

### <span data-ttu-id="55b7e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="55b7e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="55b7e-112">Elimina uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="55b7e-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="55b7e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55b7e-113">PARAMETERS</span></span>

### <span data-ttu-id="55b7e-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55b7e-114">-Confirm</span></span>
<span data-ttu-id="55b7e-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b7e-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b7e-116">-DefaultProfile</span></span>
<span data-ttu-id="55b7e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55b7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-118">-ID</span><span class="sxs-lookup"><span data-stu-id="55b7e-118">-Id</span></span>
<span data-ttu-id="55b7e-119">ID risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="55b7e-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="55b7e-120">Esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="55b7e-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55b7e-121">-InputObject</span></span>
<span data-ttu-id="55b7e-122">Oggetto PowerShell per lo script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="55b7e-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="55b7e-123">-Name</span></span>
<span data-ttu-id="55b7e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55b7e-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55b7e-125">-PassThru</span></span>
<span data-ttu-id="55b7e-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="55b7e-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="55b7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="55b7e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55b7e-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b7e-129">-WhatIf</span></span>
<span data-ttu-id="55b7e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55b7e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b7e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55b7e-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55b7e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b7e-132">CommonParameters</span></span>
<span data-ttu-id="55b7e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b7e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="55b7e-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b7e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b7e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55b7e-135">INPUTS</span></span>

### <span data-ttu-id="55b7e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="55b7e-136">System.String</span></span>

### <span data-ttu-id="55b7e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="55b7e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="55b7e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55b7e-138">OUTPUTS</span></span>

### <span data-ttu-id="55b7e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="55b7e-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="55b7e-140">Note</span><span class="sxs-lookup"><span data-stu-id="55b7e-140">NOTES</span></span>

## <span data-ttu-id="55b7e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55b7e-141">RELATED LINKS</span></span>