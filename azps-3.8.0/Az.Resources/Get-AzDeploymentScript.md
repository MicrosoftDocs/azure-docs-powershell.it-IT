---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020282"
---
# <span data-ttu-id="206e2-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="206e2-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="206e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="206e2-102">SYNOPSIS</span></span>
<span data-ttu-id="206e2-103">Ottiene o elenca gli script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="206e2-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="206e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="206e2-104">SYNTAX</span></span>

### <span data-ttu-id="206e2-105">ListDeploymentScript (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="206e2-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="206e2-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="206e2-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="206e2-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="206e2-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="206e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="206e2-108">DESCRIPTION</span></span>
<span data-ttu-id="206e2-109">Il cmdlet **Get-AzDeploymentScript** ottiene un singolo script di distribuzione o un elenco di script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="206e2-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="206e2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="206e2-110">EXAMPLES</span></span>

### <span data-ttu-id="206e2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="206e2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="206e2-112">Elenca gli script di distribuzione nell'abbonamento nel contesto dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="206e2-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="206e2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="206e2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="206e2-114">Elenca gli script di distribuzione nel gruppo di risorse DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="206e2-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="206e2-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="206e2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="206e2-116">Ottiene uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="206e2-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="206e2-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="206e2-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="206e2-118">Ottiene uno script di distribuzione con l'ID risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="206e2-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="206e2-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="206e2-119">PARAMETERS</span></span>

### <span data-ttu-id="206e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="206e2-120">-DefaultProfile</span></span>
<span data-ttu-id="206e2-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="206e2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="206e2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="206e2-122">-Id</span></span>
<span data-ttu-id="206e2-123">ID risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="206e2-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="206e2-124">Esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="206e2-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206e2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="206e2-125">-Name</span></span>
<span data-ttu-id="206e2-126">Nome dello script di distribuzione</span><span class="sxs-lookup"><span data-stu-id="206e2-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206e2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="206e2-127">-ResourceGroupName</span></span>
<span data-ttu-id="206e2-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="206e2-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="206e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="206e2-129">CommonParameters</span></span>
<span data-ttu-id="206e2-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="206e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="206e2-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="206e2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="206e2-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="206e2-132">INPUTS</span></span>

### <span data-ttu-id="206e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="206e2-133">System.String</span></span>

## <span data-ttu-id="206e2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="206e2-134">OUTPUTS</span></span>

### <span data-ttu-id="206e2-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="206e2-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="206e2-136">Note</span><span class="sxs-lookup"><span data-stu-id="206e2-136">NOTES</span></span>

## <span data-ttu-id="206e2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="206e2-137">RELATED LINKS</span></span>
