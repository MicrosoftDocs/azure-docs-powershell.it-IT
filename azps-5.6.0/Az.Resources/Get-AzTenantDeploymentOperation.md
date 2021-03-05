---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: cf48e14ded4dd227cb241a341339861bae3a269a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997203"
---
# <span data-ttu-id="d6443-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d6443-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="d6443-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6443-102">SYNOPSIS</span></span>
<span data-ttu-id="d6443-103">Ottenere l'operazione di distribuzione per la distribuzione nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="d6443-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="d6443-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6443-104">SYNTAX</span></span>

### <span data-ttu-id="d6443-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6443-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6443-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d6443-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6443-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d6443-107">DESCRIPTION</span></span>
<span data-ttu-id="d6443-108">Il cmdlet **Get-AzTenantDeploymentOperation** elenca tutte le operazioni che erano parte della distribuzione nell'ambito tenant corrente per identificare e fornire altre informazioni sulle esatte operazioni non riuscite per una particolare distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d6443-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="d6443-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6443-109">EXAMPLES</span></span>

### <span data-ttu-id="d6443-110">Esempio 1: Ottenere le operazioni di distribuzione con un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="d6443-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="d6443-111">Ottiene le operazioni di distribuzione con il nome "Deploy01" nell'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="d6443-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="d6443-112">Esempio 2: Ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="d6443-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="d6443-113">Questo comando recupera la distribuzione "Deploy01" nell'ambito tenant corrente e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d6443-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="d6443-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6443-114">PARAMETERS</span></span>

### <span data-ttu-id="d6443-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6443-115">-DefaultProfile</span></span>
<span data-ttu-id="d6443-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6443-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6443-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d6443-117">-DeploymentName</span></span>
<span data-ttu-id="d6443-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d6443-118">The deployment name.</span></span>

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

### <span data-ttu-id="d6443-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d6443-119">-DeploymentObject</span></span>
<span data-ttu-id="d6443-120">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d6443-120">The deployment object.</span></span>

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

### <span data-ttu-id="d6443-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d6443-121">-OperationId</span></span>
<span data-ttu-id="d6443-122">ID dell'operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d6443-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="d6443-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6443-123">-Pre</span></span>
<span data-ttu-id="d6443-124">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d6443-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d6443-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6443-125">CommonParameters</span></span>
<span data-ttu-id="d6443-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6443-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6443-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6443-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6443-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="d6443-128">INPUTS</span></span>

### <span data-ttu-id="d6443-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d6443-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d6443-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6443-130">OUTPUTS</span></span>

### <span data-ttu-id="d6443-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d6443-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d6443-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="d6443-132">NOTES</span></span>

## <span data-ttu-id="d6443-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6443-133">RELATED LINKS</span></span>
