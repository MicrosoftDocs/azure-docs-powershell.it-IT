---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192759"
---
# <span data-ttu-id="5bfa9-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5bfa9-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="5bfa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfa9-103">Ottenere l'operazione di distribuzione per la distribuzione nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="5bfa9-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="5bfa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bfa9-104">SYNTAX</span></span>

### <span data-ttu-id="5bfa9-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5bfa9-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bfa9-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5bfa9-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bfa9-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5bfa9-107">DESCRIPTION</span></span>
<span data-ttu-id="5bfa9-108">Il cmdlet **Get-AzTenantDeploymentOperation** elenca tutte le operazioni che erano parte della distribuzione nell'ambito tenant corrente per identificare e fornire altre informazioni sulle esatte operazioni non riuscite per una particolare distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="5bfa9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bfa9-109">EXAMPLES</span></span>

### <span data-ttu-id="5bfa9-110">Esempio 1: Ottenere le operazioni di distribuzione con un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="5bfa9-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="5bfa9-111">Ottiene le operazioni di distribuzione con il nome "Deploy01" nell'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="5bfa9-112">Esempio 2: Ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="5bfa9-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="5bfa9-113">Questo comando recupera la distribuzione "Deploy01" nell'ambito tenant corrente e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="5bfa9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bfa9-114">PARAMETERS</span></span>

### <span data-ttu-id="5bfa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfa9-115">-DefaultProfile</span></span>
<span data-ttu-id="5bfa9-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bfa9-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5bfa9-117">-DeploymentName</span></span>
<span data-ttu-id="5bfa9-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-118">The deployment name.</span></span>

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

### <span data-ttu-id="5bfa9-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5bfa9-119">-DeploymentObject</span></span>
<span data-ttu-id="5bfa9-120">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-120">The deployment object.</span></span>

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

### <span data-ttu-id="5bfa9-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5bfa9-121">-OperationId</span></span>
<span data-ttu-id="5bfa9-122">ID dell'operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="5bfa9-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bfa9-123">-Pre</span></span>
<span data-ttu-id="5bfa9-124">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5bfa9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfa9-125">CommonParameters</span></span>
<span data-ttu-id="5bfa9-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfa9-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5bfa9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfa9-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="5bfa9-128">INPUTS</span></span>

### <span data-ttu-id="5bfa9-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5bfa9-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5bfa9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bfa9-130">OUTPUTS</span></span>

### <span data-ttu-id="5bfa9-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="5bfa9-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="5bfa9-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="5bfa9-132">NOTES</span></span>

## <span data-ttu-id="5bfa9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bfa9-133">RELATED LINKS</span></span>
