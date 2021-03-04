---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 36bb1f153ea55024227c2198d27006f6ed3069d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958030"
---
# <span data-ttu-id="22c4a-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="22c4a-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="22c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="22c4a-103">Ottenere l'operazione di distribuzione per la distribuzione dei gruppi di gestione</span><span class="sxs-lookup"><span data-stu-id="22c4a-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="22c4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22c4a-104">SYNTAX</span></span>

### <span data-ttu-id="22c4a-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22c4a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22c4a-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="22c4a-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22c4a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22c4a-107">DESCRIPTION</span></span>
<span data-ttu-id="22c4a-108">Il cmdlet **Get-AzManagementGroupDeploymentOperation** elenca tutte le operazioni che fanno parte di una distribuzione del gruppo di gestione per identificare e fornire altre informazioni sulle esatte operazioni non riuscite per una particolare distribuzione.</span><span class="sxs-lookup"><span data-stu-id="22c4a-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="22c4a-109">Si tratta delle stesse informazioni fornite nei dettagli della distribuzione nel portale.</span><span class="sxs-lookup"><span data-stu-id="22c4a-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="22c4a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22c4a-110">EXAMPLES</span></span>

### <span data-ttu-id="22c4a-111">Esempio 1: Ottenere le operazioni di distribuzione con un nome di distribuzione</span><span class="sxs-lookup"><span data-stu-id="22c4a-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="22c4a-112">Recupera le operazioni di distribuzione con il nome "Deploy01" al gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="22c4a-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="22c4a-113">Esempio 2: Ottenere una distribuzione e ottenere le operazioni di distribuzione</span><span class="sxs-lookup"><span data-stu-id="22c4a-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="22c4a-114">Questo comando recupera la distribuzione "Deploy01" presso il gruppo di gestione "myMG" e ottiene le operazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="22c4a-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="22c4a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22c4a-115">PARAMETERS</span></span>

### <span data-ttu-id="22c4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c4a-116">-DefaultProfile</span></span>
<span data-ttu-id="22c4a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22c4a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c4a-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="22c4a-118">-DeploymentName</span></span>
<span data-ttu-id="22c4a-119">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="22c4a-119">The deployment name.</span></span>

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

### <span data-ttu-id="22c4a-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="22c4a-120">-DeploymentObject</span></span>
<span data-ttu-id="22c4a-121">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="22c4a-121">The deployment object.</span></span>

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

### <span data-ttu-id="22c4a-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="22c4a-122">-ManagementGroupId</span></span>
<span data-ttu-id="22c4a-123">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="22c4a-123">The management group id.</span></span>

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

### <span data-ttu-id="22c4a-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="22c4a-124">-OperationId</span></span>
<span data-ttu-id="22c4a-125">ID dell'operazione di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="22c4a-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="22c4a-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="22c4a-126">-Pre</span></span>
<span data-ttu-id="22c4a-127">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="22c4a-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="22c4a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c4a-128">CommonParameters</span></span>
<span data-ttu-id="22c4a-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c4a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c4a-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22c4a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c4a-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="22c4a-131">INPUTS</span></span>

### <span data-ttu-id="22c4a-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="22c4a-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="22c4a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22c4a-133">OUTPUTS</span></span>

### <span data-ttu-id="22c4a-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="22c4a-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="22c4a-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="22c4a-135">NOTES</span></span>

## <span data-ttu-id="22c4a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22c4a-136">RELATED LINKS</span></span>
