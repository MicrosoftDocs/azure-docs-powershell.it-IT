---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 9904dc21f4c37c36684d2c74e97486c1a516aa88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190640"
---
# <span data-ttu-id="042ed-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="042ed-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="042ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="042ed-102">SYNOPSIS</span></span>
<span data-ttu-id="042ed-103">Rimuove uno script di distribuzione e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="042ed-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="042ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="042ed-104">SYNTAX</span></span>

### <span data-ttu-id="042ed-105">RemoveDeploymentScriptLogByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="042ed-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="042ed-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="042ed-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="042ed-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="042ed-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="042ed-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="042ed-108">DESCRIPTION</span></span>
<span data-ttu-id="042ed-109">Il cmdlet **Remove-AzDeploymentScript** rimuove uno script di distribuzione e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="042ed-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="042ed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="042ed-110">EXAMPLES</span></span>

### <span data-ttu-id="042ed-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="042ed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="042ed-112">Elimina uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="042ed-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="042ed-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="042ed-113">PARAMETERS</span></span>

### <span data-ttu-id="042ed-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="042ed-114">-Confirm</span></span>
<span data-ttu-id="042ed-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="042ed-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="042ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042ed-116">-DefaultProfile</span></span>
<span data-ttu-id="042ed-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="042ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="042ed-118">-ID</span><span class="sxs-lookup"><span data-stu-id="042ed-118">-Id</span></span>
<span data-ttu-id="042ed-119">ID risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="042ed-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="042ed-120">Esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="042ed-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="042ed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="042ed-121">-InputObject</span></span>
<span data-ttu-id="042ed-122">Oggetto PowerShell per lo script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="042ed-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="042ed-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="042ed-123">-Name</span></span>
<span data-ttu-id="042ed-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="042ed-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="042ed-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="042ed-125">-PassThru</span></span>
<span data-ttu-id="042ed-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="042ed-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="042ed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042ed-127">-ResourceGroupName</span></span>
<span data-ttu-id="042ed-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="042ed-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="042ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="042ed-129">-WhatIf</span></span>
<span data-ttu-id="042ed-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="042ed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="042ed-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="042ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="042ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042ed-132">CommonParameters</span></span>
<span data-ttu-id="042ed-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="042ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="042ed-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042ed-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042ed-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="042ed-135">INPUTS</span></span>

### <span data-ttu-id="042ed-136">System. String</span><span class="sxs-lookup"><span data-stu-id="042ed-136">System.String</span></span>

### <span data-ttu-id="042ed-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="042ed-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="042ed-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="042ed-138">OUTPUTS</span></span>

### <span data-ttu-id="042ed-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="042ed-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="042ed-140">Note</span><span class="sxs-lookup"><span data-stu-id="042ed-140">NOTES</span></span>

## <span data-ttu-id="042ed-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="042ed-141">RELATED LINKS</span></span>
