---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023153"
---
# <span data-ttu-id="ee5e1-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="ee5e1-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="ee5e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5e1-103">Ottenere una posizione di aggiornamento in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-103">Get an update location based on name.</span></span>

## <span data-ttu-id="ee5e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee5e1-104">SYNTAX</span></span>

### <span data-ttu-id="ee5e1-105">Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee5e1-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee5e1-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee5e1-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee5e1-107">Elenco</span><span class="sxs-lookup"><span data-stu-id="ee5e1-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee5e1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee5e1-108">DESCRIPTION</span></span>
<span data-ttu-id="ee5e1-109">Ottenere una posizione di aggiornamento in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-109">Get an update location based on name.</span></span>

## <span data-ttu-id="ee5e1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee5e1-110">EXAMPLES</span></span>

### <span data-ttu-id="ee5e1-111">Esempio 1: ottenere tutte le posizioni degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ee5e1-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="ee5e1-112">Senza parametri, questo unifiedgroup recupererà tutte le posizioni di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ee5e1-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="ee5e1-113">Esempio 2: ottenere tutti i percorsi degli aggiornamenti per nome</span><span class="sxs-lookup"><span data-stu-id="ee5e1-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="ee5e1-114">Recupererà tutti i percorsi di aggiornamento corrispondenti al parametro name specificato</span><span class="sxs-lookup"><span data-stu-id="ee5e1-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="ee5e1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee5e1-115">PARAMETERS</span></span>

### <span data-ttu-id="ee5e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5e1-116">-DefaultProfile</span></span>
<span data-ttu-id="ee5e1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee5e1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee5e1-118">-InputObject</span></span>
<span data-ttu-id="ee5e1-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="ee5e1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee5e1-120">-Name</span></span>
<span data-ttu-id="ee5e1-121">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ee5e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee5e1-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ee5e1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee5e1-124">-SubscriptionId</span></span>
<span data-ttu-id="ee5e1-125">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ee5e1-126">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ee5e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5e1-127">CommonParameters</span></span>
<span data-ttu-id="ee5e1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5e1-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee5e1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5e1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee5e1-130">INPUTS</span></span>

### <span data-ttu-id="ee5e1-131">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ee5e1-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="ee5e1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee5e1-132">OUTPUTS</span></span>

### <span data-ttu-id="ee5e1-133">Microsoft. Azure. PowerShell. Cmdlets. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="ee5e1-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="ee5e1-134">Note</span><span class="sxs-lookup"><span data-stu-id="ee5e1-134">NOTES</span></span>

<span data-ttu-id="ee5e1-135">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee5e1-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ee5e1-137">INPUTOBJECT <IUpdateAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="ee5e1-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee5e1-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="ee5e1-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee5e1-139">`[ResourceGroupName <String>]`: Nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="ee5e1-140">`[RunName <String>]`: Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="ee5e1-141">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="ee5e1-142">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ee5e1-143">`[UpdateLocation <String>]`: Nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="ee5e1-144">`[UpdateName <String>]`: Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ee5e1-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="ee5e1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee5e1-145">RELATED LINKS</span></span>

