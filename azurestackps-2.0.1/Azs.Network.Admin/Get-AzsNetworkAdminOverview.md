---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023172"
---
# <span data-ttu-id="31db5-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="31db5-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="31db5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31db5-102">SYNOPSIS</span></span>
<span data-ttu-id="31db5-103">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="31db5-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="31db5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31db5-104">SYNTAX</span></span>

### <span data-ttu-id="31db5-105">Get (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31db5-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="31db5-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="31db5-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="31db5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31db5-107">DESCRIPTION</span></span>
<span data-ttu-id="31db5-108">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="31db5-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="31db5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31db5-109">EXAMPLES</span></span>

### <span data-ttu-id="31db5-110">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="31db5-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="31db5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31db5-111">PARAMETERS</span></span>

### <span data-ttu-id="31db5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31db5-112">-DefaultProfile</span></span>
<span data-ttu-id="31db5-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31db5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31db5-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31db5-114">-InputObject</span></span>
<span data-ttu-id="31db5-115">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="31db5-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="31db5-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31db5-116">-SubscriptionId</span></span>
<span data-ttu-id="31db5-117">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="31db5-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="31db5-118">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="31db5-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="31db5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31db5-119">CommonParameters</span></span>
<span data-ttu-id="31db5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31db5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31db5-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31db5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31db5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31db5-122">INPUTS</span></span>

### <span data-ttu-id="31db5-123">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="31db5-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="31db5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31db5-124">OUTPUTS</span></span>

### <span data-ttu-id="31db5-125">Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="31db5-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="31db5-126">Note</span><span class="sxs-lookup"><span data-stu-id="31db5-126">NOTES</span></span>

<span data-ttu-id="31db5-127">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="31db5-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31db5-128">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31db5-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="31db5-129">INPUTOBJECT <INetworkAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="31db5-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31db5-130">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="31db5-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31db5-131">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="31db5-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="31db5-132">`[ResourceName <String>]`: Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="31db5-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="31db5-133">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="31db5-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="31db5-134">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="31db5-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="31db5-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31db5-135">RELATED LINKS</span></span>

