---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478051"
---
# <span data-ttu-id="c9b58-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="c9b58-101">Get-AzBotService</span></span>

## <span data-ttu-id="c9b58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9b58-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b58-103">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="c9b58-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c9b58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9b58-104">SYNTAX</span></span>

### <span data-ttu-id="c9b58-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9b58-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9b58-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c9b58-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9b58-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9b58-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9b58-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="c9b58-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9b58-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9b58-109">DESCRIPTION</span></span>
<span data-ttu-id="c9b58-110">Restituisce un BotService specificato dai parametri.</span><span class="sxs-lookup"><span data-stu-id="c9b58-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c9b58-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9b58-111">EXAMPLES</span></span>

### <span data-ttu-id="c9b58-112">Esempio 1: ottenere tutti BotServices</span><span class="sxs-lookup"><span data-stu-id="c9b58-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="c9b58-113">Ottenere tutti BotServices</span><span class="sxs-lookup"><span data-stu-id="c9b58-113">Get all BotServices</span></span>

### <span data-ttu-id="c9b58-114">Esempio 2: ottenere il BotService in base a ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="c9b58-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="c9b58-115">Ottenere il BotService per ResourceGroupName e nome</span><span class="sxs-lookup"><span data-stu-id="c9b58-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="c9b58-116">Esempio 3: ottenere tutte le BotServices da ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b58-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="c9b58-117">Ottenere tutti i BotServices da ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b58-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="c9b58-118">Esempio 4: ottenere il BotService da inputObject</span><span class="sxs-lookup"><span data-stu-id="c9b58-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="c9b58-119">Ottenere il BotService da inputObject</span><span class="sxs-lookup"><span data-stu-id="c9b58-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="c9b58-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9b58-120">PARAMETERS</span></span>

### <span data-ttu-id="c9b58-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b58-121">-DefaultProfile</span></span>
<span data-ttu-id="c9b58-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b58-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b58-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9b58-123">-InputObject</span></span>
<span data-ttu-id="c9b58-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c9b58-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b58-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9b58-125">-Name</span></span>
<span data-ttu-id="c9b58-126">Il nome della risorsa bot.</span><span class="sxs-lookup"><span data-stu-id="c9b58-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b58-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9b58-128">Nome del gruppo di risorse bot nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="c9b58-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="c9b58-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9b58-129">-SubscriptionId</span></span>
<span data-ttu-id="c9b58-130">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b58-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c9b58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b58-131">CommonParameters</span></span>
<span data-ttu-id="c9b58-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b58-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9b58-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b58-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9b58-134">INPUTS</span></span>

### <span data-ttu-id="c9b58-135">Microsoft. Azure. PowerShell. Cmdlets. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c9b58-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="c9b58-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9b58-136">OUTPUTS</span></span>

### <span data-ttu-id="c9b58-137">Microsoft. Azure. PowerShell. Cmdlets. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="c9b58-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="c9b58-138">Note</span><span class="sxs-lookup"><span data-stu-id="c9b58-138">NOTES</span></span>

<span data-ttu-id="c9b58-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c9b58-139">ALIASES</span></span>

<span data-ttu-id="c9b58-140">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9b58-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9b58-141">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c9b58-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9b58-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9b58-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9b58-143">INPUTOBJECT <IBotServiceIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c9b58-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9b58-144">`[ChannelName <ChannelName?>]`: Il nome della risorsa canale.</span><span class="sxs-lookup"><span data-stu-id="c9b58-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="c9b58-145">`[ConnectionName <String>]`: Il nome della risorsa di impostazione della connessione al servizio bot</span><span class="sxs-lookup"><span data-stu-id="c9b58-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="c9b58-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c9b58-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9b58-147">`[ResourceGroupName <String>]`: Nome del gruppo di risorse bot nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="c9b58-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="c9b58-148">`[ResourceName <String>]`: Il nome della risorsa bot.</span><span class="sxs-lookup"><span data-stu-id="c9b58-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="c9b58-149">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b58-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c9b58-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9b58-150">RELATED LINKS</span></span>

