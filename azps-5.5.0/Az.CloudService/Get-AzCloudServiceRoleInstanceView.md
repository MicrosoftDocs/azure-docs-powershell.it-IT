---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceView.md
ms.openlocfilehash: a86ebbda321f37a38b3d014377081087f37feb9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181791"
---
# <span data-ttu-id="03856-101">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="03856-101">Get-AzCloudServiceRoleInstanceView</span></span>

## <span data-ttu-id="03856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03856-102">SYNOPSIS</span></span>
<span data-ttu-id="03856-103">Recupera informazioni sullo stato di esecuzione di un'istanza del ruolo in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="03856-103">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="03856-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03856-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="03856-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03856-105">DESCRIPTION</span></span>
<span data-ttu-id="03856-106">Recupera informazioni sullo stato di esecuzione di un'istanza del ruolo in un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="03856-106">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

## <span data-ttu-id="03856-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03856-107">EXAMPLES</span></span>

### <span data-ttu-id="03856-108">Esempio 1: Ottenere i dettagli della visualizzazione istanza per l'istanza del ruolo servizio cloud</span><span class="sxs-lookup"><span data-stu-id="03856-108">Example 1: Get instance view details for cloud service role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Statuses           PlatformFaultDomain PlatformUpdateDomain
--------           ------------------- --------------------
{RoleStateStarted} 0                   0

```

<span data-ttu-id="03856-109">Questo cmdlet ottiene la visualizzazione dell'istanza del ruolo denominata ContosoFrontEnd_IN_0 del servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="03856-109">This cmdlet gets the instance view of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="03856-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03856-110">PARAMETERS</span></span>

### <span data-ttu-id="03856-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="03856-111">-CloudServiceName</span></span>
<span data-ttu-id="03856-112">.</span><span class="sxs-lookup"><span data-stu-id="03856-112">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03856-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03856-113">-DefaultProfile</span></span>
<span data-ttu-id="03856-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03856-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03856-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03856-115">-ResourceGroupName</span></span>
<span data-ttu-id="03856-116">.</span><span class="sxs-lookup"><span data-stu-id="03856-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03856-117">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="03856-117">-RoleInstanceName</span></span>
<span data-ttu-id="03856-118">Nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="03856-118">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03856-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03856-119">-SubscriptionId</span></span>
<span data-ttu-id="03856-120">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="03856-120">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="03856-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="03856-121">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03856-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03856-122">CommonParameters</span></span>
<span data-ttu-id="03856-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03856-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03856-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03856-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03856-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="03856-125">INPUTS</span></span>

## <span data-ttu-id="03856-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03856-126">OUTPUTS</span></span>

### <span data-ttu-id="03856-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="03856-127">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstanceView</span></span>

## <span data-ttu-id="03856-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="03856-128">NOTES</span></span>

<span data-ttu-id="03856-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="03856-129">ALIASES</span></span>

## <span data-ttu-id="03856-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03856-130">RELATED LINKS</span></span>

