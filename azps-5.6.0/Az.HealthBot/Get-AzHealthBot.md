---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013230"
---
# <span data-ttu-id="8a6bd-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="8a6bd-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="8a6bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6bd-103">Ottieni il bot della salute.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-103">Get a HealthBot.</span></span>

## <span data-ttu-id="8a6bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a6bd-104">SYNTAX</span></span>

### <span data-ttu-id="8a6bd-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a6bd-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a6bd-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8a6bd-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a6bd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a6bd-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a6bd-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="8a6bd-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a6bd-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8a6bd-109">DESCRIPTION</span></span>
<span data-ttu-id="8a6bd-110">Ottieni il bot della salute.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-110">Get a HealthBot.</span></span>

## <span data-ttu-id="8a6bd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a6bd-111">EXAMPLES</span></span>

### <span data-ttu-id="8a6bd-112">Esempio 1: Scarica tutti i bot della salute</span><span class="sxs-lookup"><span data-stu-id="8a6bd-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="8a6bd-113">Scarica tutti HealthBot</span><span class="sxs-lookup"><span data-stu-id="8a6bd-113">Get all HealthBot</span></span>

### <span data-ttu-id="8a6bd-114">Esempio 2: Ottenere tutti i messaggi healthBot per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6bd-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="8a6bd-115">Ottieni tutto HealthBot per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6bd-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="8a6bd-116">Esempio 3: Ottenere HealthBot per NomeGruppo Risorse e Nome</span><span class="sxs-lookup"><span data-stu-id="8a6bd-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="8a6bd-117">Ottenere HealthBot per NomeGruppo Risorse e Nome</span><span class="sxs-lookup"><span data-stu-id="8a6bd-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="8a6bd-118">Esempio 4: Ottenere HealthBot da InputObject</span><span class="sxs-lookup"><span data-stu-id="8a6bd-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="8a6bd-119">Ottenere HealthBot da InputObject</span><span class="sxs-lookup"><span data-stu-id="8a6bd-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="8a6bd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a6bd-120">PARAMETERS</span></span>

### <span data-ttu-id="8a6bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6bd-121">-DefaultProfile</span></span>
<span data-ttu-id="8a6bd-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6bd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a6bd-123">-InputObject</span></span>
<span data-ttu-id="8a6bd-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6bd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8a6bd-125">-Name</span></span>
<span data-ttu-id="8a6bd-126">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="8a6bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a6bd-128">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="8a6bd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a6bd-129">-SubscriptionId</span></span>
<span data-ttu-id="8a6bd-130">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8a6bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6bd-131">CommonParameters</span></span>
<span data-ttu-id="8a6bd-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6bd-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6bd-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="8a6bd-134">INPUTS</span></span>

### <span data-ttu-id="8a6bd-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="8a6bd-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="8a6bd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a6bd-136">OUTPUTS</span></span>

### <span data-ttu-id="8a6bd-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="8a6bd-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="8a6bd-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="8a6bd-138">NOTES</span></span>

<span data-ttu-id="8a6bd-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="8a6bd-139">ALIASES</span></span>

<span data-ttu-id="8a6bd-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="8a6bd-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a6bd-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a6bd-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a6bd-143">INPUTOBJECT <IHealthBotIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="8a6bd-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a6bd-144">`[BotName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="8a6bd-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="8a6bd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a6bd-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="8a6bd-147">`[SubscriptionId <String>]`: ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6bd-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="8a6bd-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a6bd-148">RELATED LINKS</span></span>

