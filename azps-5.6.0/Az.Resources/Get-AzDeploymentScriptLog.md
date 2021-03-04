---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: dc62e4766a83e1a2046b15fbdf6619e08c4b8e28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956637"
---
# <span data-ttu-id="c97b6-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c97b6-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c97b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c97b6-102">SYNOPSIS</span></span>
<span data-ttu-id="c97b6-103">Ottiene il log di esecuzione di uno script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c97b6-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c97b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c97b6-104">SYNTAX</span></span>

### <span data-ttu-id="c97b6-105">GetDeploymentScriptLogByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c97b6-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c97b6-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c97b6-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c97b6-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c97b6-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c97b6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c97b6-108">DESCRIPTION</span></span>
<span data-ttu-id="c97b6-109">Il cmdlet **Get-AzDeploymentScriptLog** ottiene il log di un'esecuzione dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c97b6-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c97b6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c97b6-110">EXAMPLES</span></span>

### <span data-ttu-id="c97b6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c97b6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="c97b6-112">Ottiene il log di uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c97b6-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c97b6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c97b6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="c97b6-114">Ottiene le ultime 3 righe del log di uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c97b6-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c97b6-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c97b6-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="c97b6-116">Il primo comando ottiene uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c97b6-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="c97b6-117">Il secondo comando ottiene il log dello script di distribuzione specificato.</span><span class="sxs-lookup"><span data-stu-id="c97b6-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="c97b6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c97b6-118">PARAMETERS</span></span>

### <span data-ttu-id="c97b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97b6-119">-DefaultProfile</span></span>
<span data-ttu-id="c97b6-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c97b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97b6-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="c97b6-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="c97b6-122">Oggetto PowerShell dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c97b6-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b6-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="c97b6-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c97b6-124">ID di risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c97b6-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c97b6-125">Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c97b6-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c97b6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c97b6-126">-Name</span></span>
<span data-ttu-id="c97b6-127">Nome dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c97b6-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="c97b6-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c97b6-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b6-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="c97b6-130">-Tail</span></span>
<span data-ttu-id="c97b6-131">Limita l'output alle ultime n righe</span><span class="sxs-lookup"><span data-stu-id="c97b6-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c97b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97b6-132">CommonParameters</span></span>
<span data-ttu-id="c97b6-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97b6-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c97b6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97b6-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="c97b6-135">INPUTS</span></span>

### <span data-ttu-id="c97b6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c97b6-136">System.String</span></span>

### <span data-ttu-id="c97b6-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c97b6-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="c97b6-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c97b6-138">OUTPUTS</span></span>

### <span data-ttu-id="c97b6-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c97b6-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="c97b6-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="c97b6-140">NOTES</span></span>

## <span data-ttu-id="c97b6-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c97b6-141">RELATED LINKS</span></span>
