---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: 19ae45bf50c9ae54075e46a8db8fc66cc08e488a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997036"
---
# <span data-ttu-id="152f4-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="152f4-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="152f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="152f4-102">SYNOPSIS</span></span>
<span data-ttu-id="152f4-103">L'operazione Ottieni servizio di dominio recupera una rappresentazione json del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="152f4-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="152f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="152f4-104">SYNTAX</span></span>

### <span data-ttu-id="152f4-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="152f4-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="152f4-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="152f4-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="152f4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="152f4-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="152f4-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="152f4-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="152f4-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="152f4-109">DESCRIPTION</span></span>
<span data-ttu-id="152f4-110">L'operazione Get Domain Service recupera una rappresentazione json del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="152f4-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="152f4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="152f4-111">EXAMPLES</span></span>

### <span data-ttu-id="152f4-112">Esempio 1: Ottenere tutto ADDomainService per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="152f4-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="152f4-113">Ottieni All ADDomainService per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="152f4-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="152f4-114">Esempio 2: Ottenere ADDomainService By ResourceGroup e il nome</span><span class="sxs-lookup"><span data-stu-id="152f4-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="152f4-115">Ottenere ADDomainService per nome e gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="152f4-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="152f4-116">Esempio 3: Ottenere tutti ADDomainService By ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="152f4-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="152f4-117">Ottenere tutti ADDomainService Per ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="152f4-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="152f4-118">Esempio 4: Ottenere ADDomainService da InputObject</span><span class="sxs-lookup"><span data-stu-id="152f4-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="152f4-119">Ottenere ADDomainService per InputObject</span><span class="sxs-lookup"><span data-stu-id="152f4-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="152f4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="152f4-120">PARAMETERS</span></span>

### <span data-ttu-id="152f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152f4-121">-DefaultProfile</span></span>
<span data-ttu-id="152f4-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="152f4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152f4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="152f4-123">-InputObject</span></span>
<span data-ttu-id="152f4-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="152f4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="152f4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="152f4-125">-Name</span></span>
<span data-ttu-id="152f4-126">Nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="152f4-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152f4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152f4-127">-ResourceGroupName</span></span>
<span data-ttu-id="152f4-128">Nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="152f4-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="152f4-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="152f4-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="152f4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="152f4-130">-SubscriptionId</span></span>
<span data-ttu-id="152f4-131">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="152f4-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="152f4-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="152f4-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="152f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152f4-133">CommonParameters</span></span>
<span data-ttu-id="152f4-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="152f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152f4-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="152f4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152f4-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="152f4-136">INPUTS</span></span>

### <span data-ttu-id="152f4-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="152f4-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="152f4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="152f4-138">OUTPUTS</span></span>

### <span data-ttu-id="152f4-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="152f4-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="152f4-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="152f4-140">NOTES</span></span>

<span data-ttu-id="152f4-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="152f4-141">ALIASES</span></span>

<span data-ttu-id="152f4-142">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="152f4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="152f4-143">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="152f4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="152f4-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="152f4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="152f4-145">INPUTOBJECT <IAdDomainServicesIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="152f4-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="152f4-146">`[DomainServiceName <String>]`: nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="152f4-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="152f4-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="152f4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="152f4-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="152f4-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="152f4-149">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="152f4-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="152f4-150">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="152f4-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="152f4-151">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="152f4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="152f4-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="152f4-152">RELATED LINKS</span></span>

