---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012590"
---
# <span data-ttu-id="cd264-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="cd264-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="cd264-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd264-102">SYNOPSIS</span></span>
<span data-ttu-id="cd264-103">Ottenere le proprietà di una specifica risorsa dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="cd264-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="cd264-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd264-104">SYNTAX</span></span>

### <span data-ttu-id="cd264-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd264-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd264-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cd264-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd264-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd264-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd264-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="cd264-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cd264-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd264-109">DESCRIPTION</span></span>
<span data-ttu-id="cd264-110">Ottenere le proprietà di una specifica risorsa dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="cd264-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="cd264-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd264-111">EXAMPLES</span></span>

### <span data-ttu-id="cd264-112">Esempio 1: Elencare tutte le organizzazioni confluenti sotto un abbonamento</span><span class="sxs-lookup"><span data-stu-id="cd264-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="cd264-113">Questo comando elenca tutte le organizzazioni confluenti sotto un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cd264-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="cd264-114">Esempio 2: Elencare tutte le organizzazioni confluenti in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cd264-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="cd264-115">Questo comando elenca tutte le organizzazioni confluenti in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd264-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="cd264-116">Esempio 3: Ottenere un'organizzazione confluente in base al nome</span><span class="sxs-lookup"><span data-stu-id="cd264-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="cd264-117">Questo comando ottiene un'organizzazione confluente in base al nome.</span><span class="sxs-lookup"><span data-stu-id="cd264-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="cd264-118">Esempio 4: Ottenere un'organizzazione confluente tramite pipeline</span><span class="sxs-lookup"><span data-stu-id="cd264-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="cd264-119">Questo comando ottiene un'organizzazione confluente tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd264-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="cd264-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd264-120">PARAMETERS</span></span>

### <span data-ttu-id="cd264-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd264-121">-DefaultProfile</span></span>
<span data-ttu-id="cd264-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd264-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd264-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd264-123">-InputObject</span></span>
<span data-ttu-id="cd264-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd264-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd264-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cd264-125">-Name</span></span>
<span data-ttu-id="cd264-126">Nome risorsa organizzazione</span><span class="sxs-lookup"><span data-stu-id="cd264-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd264-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd264-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd264-128">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cd264-128">Resource group name</span></span>

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

### <span data-ttu-id="cd264-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd264-129">-SubscriptionId</span></span>
<span data-ttu-id="cd264-130">ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd264-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="cd264-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd264-131">CommonParameters</span></span>
<span data-ttu-id="cd264-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd264-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd264-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd264-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd264-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd264-134">INPUTS</span></span>

### <span data-ttu-id="cd264-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="cd264-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="cd264-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd264-136">OUTPUTS</span></span>

### <span data-ttu-id="cd264-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="cd264-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="cd264-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd264-138">NOTES</span></span>

<span data-ttu-id="cd264-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd264-139">ALIASES</span></span>

<span data-ttu-id="cd264-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="cd264-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd264-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cd264-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd264-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd264-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd264-143">INPUTOBJECT <IConfluentIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cd264-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd264-144">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="cd264-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd264-145">`[OrganizationName <String>]`: nome della risorsa dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="cd264-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="cd264-146">`[ResourceGroupName <String>]`: nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cd264-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="cd264-147">`[SubscriptionId <String>]`: ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="cd264-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="cd264-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd264-148">RELATED LINKS</span></span>

