---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474240"
---
# <span data-ttu-id="2a77c-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2a77c-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="2a77c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a77c-102">SYNOPSIS</span></span>
<span data-ttu-id="2a77c-103">Ottenere l'operazione di distribuzione per la distribuzione in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="2a77c-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="2a77c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a77c-104">SYNTAX</span></span>

### <span data-ttu-id="2a77c-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a77c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a77c-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="2a77c-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a77c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a77c-107">DESCRIPTION</span></span>
<span data-ttu-id="2a77c-108">Il cmdlet **Get-AzTenantDeploymentOperation** elenca tutte le operazioni che facevano parte della distribuzione nell'ambito del tenant corrente per identificare e fornire altre informazioni sulle operazioni esatte non riuscite per una specifica distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2a77c-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="2a77c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a77c-109">EXAMPLES</span></span>

### <span data-ttu-id="2a77c-110">Esempio 1: ottenere le operazioni di distribuzione in base a un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="2a77c-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="2a77c-111">Ottiene le operazioni di distribuzione con il nome "Deploy01" nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="2a77c-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="2a77c-112">Esempio 2: ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="2a77c-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="2a77c-113">Questo comando ottiene la distribuzione "Deploy01" nell'ambito del tenant corrente e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2a77c-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="2a77c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a77c-114">PARAMETERS</span></span>

### <span data-ttu-id="2a77c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a77c-115">-DefaultProfile</span></span>
<span data-ttu-id="2a77c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a77c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a77c-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="2a77c-117">-DeploymentName</span></span>
<span data-ttu-id="2a77c-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2a77c-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a77c-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="2a77c-119">-DeploymentObject</span></span>
<span data-ttu-id="2a77c-120">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="2a77c-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a77c-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="2a77c-121">-OperationId</span></span>
<span data-ttu-id="2a77c-122">ID operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="2a77c-122">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a77c-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a77c-123">-Pre</span></span>
<span data-ttu-id="2a77c-124">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="2a77c-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2a77c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a77c-125">CommonParameters</span></span>
<span data-ttu-id="2a77c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a77c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a77c-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a77c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a77c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a77c-128">INPUTS</span></span>

### <span data-ttu-id="2a77c-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="2a77c-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="2a77c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a77c-130">OUTPUTS</span></span>

### <span data-ttu-id="2a77c-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2a77c-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="2a77c-132">Note</span><span class="sxs-lookup"><span data-stu-id="2a77c-132">NOTES</span></span>

## <span data-ttu-id="2a77c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a77c-133">RELATED LINKS</span></span>
