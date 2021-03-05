---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 516bc63d7866ffd8a3c16fd224a49697c0cc972f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001805"
---
# <span data-ttu-id="2a925-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="2a925-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="2a925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a925-102">SYNOPSIS</span></span>
<span data-ttu-id="2a925-103">Ottiene un'istanza del ruolo da un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="2a925-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="2a925-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a925-104">SYNTAX</span></span>

### <span data-ttu-id="2a925-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a925-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a925-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="2a925-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a925-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a925-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2a925-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2a925-108">DESCRIPTION</span></span>
<span data-ttu-id="2a925-109">Ottiene un'istanza del ruolo da un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="2a925-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="2a925-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a925-110">EXAMPLES</span></span>

### <span data-ttu-id="2a925-111">Esempio 1: Ottenere tutte le istanze di ruolo</span><span class="sxs-lookup"><span data-stu-id="2a925-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="2a925-112">Questo comando ottiene le proprietà di tutte le istanze di ruoli del servizio cloud denominate ContosoCS che appartengono al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="2a925-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="2a925-113">Esempio 2: Ottenere le proprietà per una singola istanza del ruolo</span><span class="sxs-lookup"><span data-stu-id="2a925-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="2a925-114">Questo comando ottiene le proprietà dell'istanza del ruolo ContosoFrontEnd_IN_0 servizio cloud denominato ContosoCS che appartiene al gruppo di risorse denominato ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="2a925-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="2a925-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a925-115">PARAMETERS</span></span>

### <span data-ttu-id="2a925-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="2a925-116">-CloudServiceName</span></span>
<span data-ttu-id="2a925-117">.</span><span class="sxs-lookup"><span data-stu-id="2a925-117">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a925-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a925-118">-DefaultProfile</span></span>
<span data-ttu-id="2a925-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a925-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a925-120">-Expand</span><span class="sxs-lookup"><span data-stu-id="2a925-120">-Expand</span></span>
<span data-ttu-id="2a925-121">Espressione di espansione da applicare all'operazione.</span><span class="sxs-lookup"><span data-stu-id="2a925-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a925-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a925-122">-InputObject</span></span>
<span data-ttu-id="2a925-123">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2a925-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a925-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a925-124">-ResourceGroupName</span></span>
<span data-ttu-id="2a925-125">.</span><span class="sxs-lookup"><span data-stu-id="2a925-125">.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a925-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="2a925-126">-RoleInstanceName</span></span>
<span data-ttu-id="2a925-127">Nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="2a925-127">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a925-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a925-128">-SubscriptionId</span></span>
<span data-ttu-id="2a925-129">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a925-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2a925-130">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2a925-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a925-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a925-131">CommonParameters</span></span>
<span data-ttu-id="2a925-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a925-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a925-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a925-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a925-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="2a925-134">INPUTS</span></span>

### <span data-ttu-id="2a925-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="2a925-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="2a925-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a925-136">OUTPUTS</span></span>

### <span data-ttu-id="2a925-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="2a925-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="2a925-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="2a925-138">NOTES</span></span>

<span data-ttu-id="2a925-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2a925-139">ALIASES</span></span>

<span data-ttu-id="2a925-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="2a925-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a925-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2a925-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a925-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a925-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a925-143">INPUTOBJECT <ICloudServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="2a925-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a925-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2a925-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="2a925-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="2a925-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a925-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2a925-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="2a925-147">`[RoleInstanceName <String>]`: nome dell'istanza del ruolo.</span><span class="sxs-lookup"><span data-stu-id="2a925-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="2a925-148">`[RoleName <String>]`: nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="2a925-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="2a925-149">`[SubscriptionId <String>]`: le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2a925-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2a925-150">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2a925-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2a925-151">`[UpdateDomain <Int32?>]`: specifica un valore intero che identifica il dominio di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2a925-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="2a925-152">I domini di aggiornamento sono identificati con un indice in base zero: il primo dominio di aggiornamento ha un ID pari a 0, il secondo con id 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="2a925-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="2a925-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a925-153">RELATED LINKS</span></span>

