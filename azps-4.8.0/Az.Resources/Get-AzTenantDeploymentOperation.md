---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191303"
---
# <span data-ttu-id="0112b-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0112b-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="0112b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0112b-102">SYNOPSIS</span></span>
<span data-ttu-id="0112b-103">Ottenere l'operazione di distribuzione per la distribuzione in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="0112b-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="0112b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0112b-104">SYNTAX</span></span>

### <span data-ttu-id="0112b-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0112b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0112b-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0112b-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0112b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0112b-107">DESCRIPTION</span></span>
<span data-ttu-id="0112b-108">Il cmdlet **Get-AzTenantDeploymentOperation** elenca tutte le operazioni che facevano parte della distribuzione nell'ambito del tenant corrente per identificare e fornire altre informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0112b-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="0112b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0112b-109">EXAMPLES</span></span>

### <span data-ttu-id="0112b-110">Esempio 1: ottenere le operazioni di distribuzione in base a un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="0112b-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="0112b-111">Ottiene le operazioni di distribuzione con il nome "Deploy01" nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="0112b-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="0112b-112">Esempio 2: ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="0112b-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="0112b-113">Questo comando ottiene la distribuzione "Deploy01" nell'ambito del tenant corrente e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0112b-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="0112b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0112b-114">PARAMETERS</span></span>

### <span data-ttu-id="0112b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0112b-115">-ApiVersion</span></span>
<span data-ttu-id="0112b-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="0112b-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0112b-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="0112b-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0112b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0112b-118">-DefaultProfile</span></span>
<span data-ttu-id="0112b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0112b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0112b-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0112b-120">-DeploymentName</span></span>
<span data-ttu-id="0112b-121">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0112b-121">The deployment name.</span></span>

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

### <span data-ttu-id="0112b-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0112b-122">-DeploymentObject</span></span>
<span data-ttu-id="0112b-123">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="0112b-123">The deployment object.</span></span>

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

### <span data-ttu-id="0112b-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0112b-124">-OperationId</span></span>
<span data-ttu-id="0112b-125">ID operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0112b-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="0112b-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="0112b-126">-Pre</span></span>
<span data-ttu-id="0112b-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0112b-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0112b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0112b-128">CommonParameters</span></span>
<span data-ttu-id="0112b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0112b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0112b-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0112b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0112b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0112b-131">INPUTS</span></span>

### <span data-ttu-id="0112b-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="0112b-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0112b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0112b-133">OUTPUTS</span></span>

### <span data-ttu-id="0112b-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0112b-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="0112b-135">Note</span><span class="sxs-lookup"><span data-stu-id="0112b-135">NOTES</span></span>

## <span data-ttu-id="0112b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0112b-136">RELATED LINKS</span></span>
