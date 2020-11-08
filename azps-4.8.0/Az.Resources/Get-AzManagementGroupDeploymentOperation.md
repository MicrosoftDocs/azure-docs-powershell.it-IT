---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192188"
---
# <span data-ttu-id="7c781-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7c781-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="7c781-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c781-102">SYNOPSIS</span></span>
<span data-ttu-id="7c781-103">Ottenere l'operazione di distribuzione per la distribuzione del gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="7c781-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="7c781-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c781-104">SYNTAX</span></span>

### <span data-ttu-id="7c781-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c781-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c781-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7c781-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c781-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c781-107">DESCRIPTION</span></span>
<span data-ttu-id="7c781-108">Il cmdlet **Get-AzManagementGroupDeploymentOperation** elenca tutte le operazioni che facevano parte di una distribuzione di un gruppo di gestione per identificare e fornire ulteriori informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7c781-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="7c781-109">Queste sono le stesse informazioni fornite nei dettagli di distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="7c781-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="7c781-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c781-110">EXAMPLES</span></span>

### <span data-ttu-id="7c781-111">Esempio 1: ottenere le operazioni di distribuzione in base a un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="7c781-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="7c781-112">Ottiene le operazioni di distribuzione con il nome "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="7c781-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="7c781-113">Esempio 2: ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="7c781-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="7c781-114">Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG" e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7c781-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="7c781-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c781-115">PARAMETERS</span></span>

### <span data-ttu-id="7c781-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c781-116">-ApiVersion</span></span>
<span data-ttu-id="7c781-117">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7c781-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c781-118">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="7c781-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c781-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c781-119">-DefaultProfile</span></span>
<span data-ttu-id="7c781-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c781-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c781-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7c781-121">-DeploymentName</span></span>
<span data-ttu-id="7c781-122">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7c781-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c781-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7c781-123">-DeploymentObject</span></span>
<span data-ttu-id="7c781-124">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="7c781-124">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c781-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7c781-125">-ManagementGroupId</span></span>
<span data-ttu-id="7c781-126">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="7c781-126">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c781-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7c781-127">-OperationId</span></span>
<span data-ttu-id="7c781-128">ID operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7c781-128">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c781-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c781-129">-Pre</span></span>
<span data-ttu-id="7c781-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7c781-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7c781-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c781-131">CommonParameters</span></span>
<span data-ttu-id="7c781-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c781-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c781-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c781-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c781-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c781-134">INPUTS</span></span>

### <span data-ttu-id="7c781-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="7c781-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7c781-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c781-136">OUTPUTS</span></span>

### <span data-ttu-id="7c781-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7c781-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="7c781-138">Note</span><span class="sxs-lookup"><span data-stu-id="7c781-138">NOTES</span></span>

## <span data-ttu-id="7c781-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c781-139">RELATED LINKS</span></span>