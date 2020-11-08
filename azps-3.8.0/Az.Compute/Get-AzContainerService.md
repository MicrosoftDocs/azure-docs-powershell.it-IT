---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021399"
---
# <span data-ttu-id="fb241-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb241-101">Get-AzContainerService</span></span>

## <span data-ttu-id="fb241-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb241-102">SYNOPSIS</span></span>
<span data-ttu-id="fb241-103">Ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="fb241-103">Gets a container service.</span></span>

## <span data-ttu-id="fb241-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb241-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb241-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb241-105">DESCRIPTION</span></span>
<span data-ttu-id="fb241-106">Il cmdlet **Get-AzContainerService** ottiene un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="fb241-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="fb241-107">È possibile visualizzare le proprietà di un servizio contenitore, che include lo stato, il numero di master e gli agenti e il nome di dominio completo di master e Agent.</span><span class="sxs-lookup"><span data-stu-id="fb241-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="fb241-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb241-108">EXAMPLES</span></span>

### <span data-ttu-id="fb241-109">Esempio 1: ottenere un servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="fb241-109">Example 1: Get a container service</span></span>
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

<span data-ttu-id="fb241-110">Questo comando ottiene un servizio contenitore denominato CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="fb241-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="fb241-111">Esempio 2: ottenere tutti i servizi contenitore</span><span class="sxs-lookup"><span data-stu-id="fb241-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="fb241-112">Questo comando consente di ottenere tutti i servizi contenitore in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fb241-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="fb241-113">Esempio 3: ottenere tutti i servizi contenitore nel gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fb241-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="fb241-114">Questo comando consente di ottenere tutti i servizi contenitore in ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="fb241-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="fb241-115">Esempio 4: ottenere tutti i servizi contenitore tramite filtro</span><span class="sxs-lookup"><span data-stu-id="fb241-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="fb241-116">Questo comando consente di ottenere tutti i servizi contenitore che iniziano con "CSResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="fb241-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="fb241-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb241-117">PARAMETERS</span></span>

### <span data-ttu-id="fb241-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb241-118">-DefaultProfile</span></span>
<span data-ttu-id="fb241-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb241-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb241-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb241-120">-Name</span></span>
<span data-ttu-id="fb241-121">Specifica il nome del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb241-121">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb241-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb241-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb241-123">Specifica il gruppo di risorse del servizio contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb241-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb241-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb241-124">CommonParameters</span></span>
<span data-ttu-id="fb241-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb241-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb241-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb241-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb241-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb241-127">INPUTS</span></span>

### <span data-ttu-id="fb241-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb241-128">System.String</span></span>

## <span data-ttu-id="fb241-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb241-129">OUTPUTS</span></span>

### <span data-ttu-id="fb241-130">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="fb241-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="fb241-131">Note</span><span class="sxs-lookup"><span data-stu-id="fb241-131">NOTES</span></span>

## <span data-ttu-id="fb241-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb241-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb241-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb241-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="fb241-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb241-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="fb241-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="fb241-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


