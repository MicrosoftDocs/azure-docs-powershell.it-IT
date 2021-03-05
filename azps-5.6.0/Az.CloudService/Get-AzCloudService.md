---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: 31683a7f8d0bea3a2e21588b0451275c74d52e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012702"
---
# <span data-ttu-id="e3a2b-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="e3a2b-101">Get-AzCloudService</span></span>

## <span data-ttu-id="e3a2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a2b-103">Visualizzare informazioni su un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="e3a2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3a2b-104">SYNTAX</span></span>

### <span data-ttu-id="e3a2b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3a2b-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3a2b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e3a2b-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3a2b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3a2b-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3a2b-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="e3a2b-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3a2b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3a2b-109">DESCRIPTION</span></span>
<span data-ttu-id="e3a2b-110">Visualizzare informazioni su un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="e3a2b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3a2b-111">EXAMPLES</span></span>

### <span data-ttu-id="e3a2b-112">Esempio 1: Ottenere tutto il servizio cloud in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e3a2b-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="e3a2b-113">Questo comando recupera tutti i servizi cloud nel gruppo di risorse denominato ContosOrg</span><span class="sxs-lookup"><span data-stu-id="e3a2b-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="e3a2b-114">Esempio 2: Ottenere il servizio cloud</span><span class="sxs-lookup"><span data-stu-id="e3a2b-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="e3a2b-115">Questo comando recupera il servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="e3a2b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3a2b-116">PARAMETERS</span></span>

### <span data-ttu-id="e3a2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a2b-117">-DefaultProfile</span></span>
<span data-ttu-id="e3a2b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a2b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3a2b-119">-InputObject</span></span>
<span data-ttu-id="e3a2b-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a2b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e3a2b-121">-Name</span></span>
<span data-ttu-id="e3a2b-122">Nome del servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a2b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a2b-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3a2b-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a2b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3a2b-125">-SubscriptionId</span></span>
<span data-ttu-id="e3a2b-126">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3a2b-127">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a2b-128">CommonParameters</span></span>
<span data-ttu-id="e3a2b-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a2b-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a2b-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3a2b-131">INPUTS</span></span>

### <span data-ttu-id="e3a2b-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e3a2b-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="e3a2b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3a2b-133">OUTPUTS</span></span>

### <span data-ttu-id="e3a2b-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="e3a2b-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="e3a2b-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3a2b-135">NOTES</span></span>

<span data-ttu-id="e3a2b-136">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e3a2b-136">ALIASES</span></span>

<span data-ttu-id="e3a2b-137">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e3a2b-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3a2b-138">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3a2b-139">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3a2b-140">INPUTOBJECT <ICloudServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e3a2b-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3a2b-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e3a2b-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="e3a2b-142">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e3a2b-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3a2b-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="e3a2b-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="e3a2b-144">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="e3a2b-145">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="e3a2b-146">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e3a2b-147">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e3a2b-148">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="e3a2b-149">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="e3a2b-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="e3a2b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3a2b-150">RELATED LINKS</span></span>

