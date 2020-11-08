---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022277"
---
# <span data-ttu-id="60fb2-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="60fb2-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="60fb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="60fb2-103">Ottiene il log di un'esecuzione dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="60fb2-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="60fb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60fb2-104">SYNTAX</span></span>

### <span data-ttu-id="60fb2-105">GetDeploymentScriptLogByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60fb2-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60fb2-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="60fb2-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60fb2-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="60fb2-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60fb2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60fb2-108">DESCRIPTION</span></span>
<span data-ttu-id="60fb2-109">Il cmdlet **Get-AzDeploymentScriptLog** ottiene il log di un'esecuzione dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="60fb2-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="60fb2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60fb2-110">EXAMPLES</span></span>

### <span data-ttu-id="60fb2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60fb2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="60fb2-112">Ottiene il log di uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="60fb2-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="60fb2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="60fb2-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="60fb2-114">Il primo comando ottiene uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="60fb2-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="60fb2-115">Il secondo comando ottiene il log dello script di distribuzione specifico.</span><span class="sxs-lookup"><span data-stu-id="60fb2-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="60fb2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60fb2-116">PARAMETERS</span></span>

### <span data-ttu-id="60fb2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60fb2-117">-DefaultProfile</span></span>
<span data-ttu-id="60fb2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60fb2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60fb2-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="60fb2-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="60fb2-120">Oggetto PowerShell per lo script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="60fb2-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60fb2-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="60fb2-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="60fb2-122">ID risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="60fb2-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="60fb2-123">Esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="60fb2-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60fb2-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="60fb2-124">-Name</span></span>
<span data-ttu-id="60fb2-125">Nome dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="60fb2-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fb2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60fb2-126">-ResourceGroupName</span></span>
<span data-ttu-id="60fb2-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60fb2-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60fb2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60fb2-128">CommonParameters</span></span>
<span data-ttu-id="60fb2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60fb2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="60fb2-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60fb2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60fb2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60fb2-131">INPUTS</span></span>

### <span data-ttu-id="60fb2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="60fb2-132">System.String</span></span>

### <span data-ttu-id="60fb2-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="60fb2-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="60fb2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60fb2-134">OUTPUTS</span></span>

### <span data-ttu-id="60fb2-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="60fb2-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="60fb2-136">Note</span><span class="sxs-lookup"><span data-stu-id="60fb2-136">NOTES</span></span>

## <span data-ttu-id="60fb2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60fb2-137">RELATED LINKS</span></span>
