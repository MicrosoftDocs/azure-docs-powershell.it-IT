---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181742"
---
# <span data-ttu-id="0bec0-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0bec0-101">Get-AzContainerService</span></span>

## <span data-ttu-id="0bec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bec0-102">SYNOPSIS</span></span>
<span data-ttu-id="0bec0-103">Ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="0bec0-103">Gets a container service.</span></span>

## <span data-ttu-id="0bec0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bec0-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bec0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0bec0-105">DESCRIPTION</span></span>
<span data-ttu-id="0bec0-106">Il cmdlet **Get-AzContainerService ottiene** un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="0bec0-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="0bec0-107">È possibile visualizzare le proprietà di un servizio contenitore, che includono lo stato, il numero di master e agenti e il nome di dominio completo di master e agente.</span><span class="sxs-lookup"><span data-stu-id="0bec0-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="0bec0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bec0-108">EXAMPLES</span></span>

### <span data-ttu-id="0bec0-109">Esempio 1: Ottenere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="0bec0-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="0bec0-110">Questo comando ottiene un servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0bec0-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="0bec0-111">Esempio 2: Ottenere tutti i servizi contenitore</span><span class="sxs-lookup"><span data-stu-id="0bec0-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="0bec0-112">Questo comando recupera tutti i servizi contenitore nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0bec0-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="0bec0-113">Esempio 3: Ottenere tutti i servizi contenitore nel gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0bec0-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="0bec0-114">Questo comando recupera tutti i servizi contenitore in ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="0bec0-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="0bec0-115">Esempio 4: Ottenere tutti i servizi contenitore con il filtro</span><span class="sxs-lookup"><span data-stu-id="0bec0-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="0bec0-116">Questo comando recupera tutti i servizi contenitore a partire da "CSResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="0bec0-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="0bec0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bec0-117">PARAMETERS</span></span>

### <span data-ttu-id="0bec0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bec0-118">-DefaultProfile</span></span>
<span data-ttu-id="0bec0-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bec0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bec0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0bec0-120">-Name</span></span>
<span data-ttu-id="0bec0-121">Specifica il nome del servizio contenitore che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bec0-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0bec0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bec0-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bec0-123">Specifica il gruppo di risorse del servizio contenitore che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bec0-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0bec0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bec0-124">CommonParameters</span></span>
<span data-ttu-id="0bec0-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bec0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bec0-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0bec0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bec0-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="0bec0-127">INPUTS</span></span>

### <span data-ttu-id="0bec0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0bec0-128">System.String</span></span>

## <span data-ttu-id="0bec0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bec0-129">OUTPUTS</span></span>

### <span data-ttu-id="0bec0-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="0bec0-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="0bec0-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="0bec0-131">NOTES</span></span>

## <span data-ttu-id="0bec0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bec0-132">RELATED LINKS</span></span>

[<span data-ttu-id="0bec0-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0bec0-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="0bec0-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0bec0-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="0bec0-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="0bec0-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


