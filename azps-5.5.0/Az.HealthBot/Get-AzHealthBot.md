---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: f7e1f596aef9169a1238f505d39f0dd201dcd8bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180582"
---
# <span data-ttu-id="ab25c-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="ab25c-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="ab25c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab25c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab25c-103">Ottieni il bot della salute.</span><span class="sxs-lookup"><span data-stu-id="ab25c-103">Get a HealthBot.</span></span>

## <span data-ttu-id="ab25c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab25c-104">SYNTAX</span></span>

### <span data-ttu-id="ab25c-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab25c-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab25c-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="ab25c-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab25c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab25c-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab25c-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="ab25c-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab25c-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ab25c-109">DESCRIPTION</span></span>
<span data-ttu-id="ab25c-110">Ottieni il bot della salute.</span><span class="sxs-lookup"><span data-stu-id="ab25c-110">Get a HealthBot.</span></span>

## <span data-ttu-id="ab25c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab25c-111">EXAMPLES</span></span>

### <span data-ttu-id="ab25c-112">Esempio 1: Scarica tutti i bot della salute</span><span class="sxs-lookup"><span data-stu-id="ab25c-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="ab25c-113">Scarica tutto HealthBot</span><span class="sxs-lookup"><span data-stu-id="ab25c-113">Get all HealthBot</span></span>

### <span data-ttu-id="ab25c-114">Esempio 2: Ottenere tutti i messaggi healthBot per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab25c-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="ab25c-115">Ottenere tutti i messaggi healthBot per ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab25c-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="ab25c-116">Esempio 3: Ottenere HealthBot per NomeGruppo Risorse e Nome</span><span class="sxs-lookup"><span data-stu-id="ab25c-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="ab25c-117">Ottenere HealthBot per NomeGruppo Risorse e Nome</span><span class="sxs-lookup"><span data-stu-id="ab25c-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="ab25c-118">Esempio 4: Ottenere HealthBot da InputObject</span><span class="sxs-lookup"><span data-stu-id="ab25c-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="ab25c-119">Ottenere HealthBot da InputObject</span><span class="sxs-lookup"><span data-stu-id="ab25c-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="ab25c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab25c-120">PARAMETERS</span></span>

### <span data-ttu-id="ab25c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab25c-121">-DefaultProfile</span></span>
<span data-ttu-id="ab25c-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab25c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab25c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab25c-123">-InputObject</span></span>
<span data-ttu-id="ab25c-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ab25c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab25c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ab25c-125">-Name</span></span>
<span data-ttu-id="ab25c-126">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="ab25c-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="ab25c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab25c-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab25c-128">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ab25c-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="ab25c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab25c-129">-SubscriptionId</span></span>
<span data-ttu-id="ab25c-130">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="ab25c-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ab25c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab25c-131">CommonParameters</span></span>
<span data-ttu-id="ab25c-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab25c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab25c-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab25c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab25c-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="ab25c-134">INPUTS</span></span>

### <span data-ttu-id="ab25c-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="ab25c-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="ab25c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab25c-136">OUTPUTS</span></span>

### <span data-ttu-id="ab25c-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="ab25c-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="ab25c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="ab25c-138">NOTES</span></span>

<span data-ttu-id="ab25c-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ab25c-139">ALIASES</span></span>

<span data-ttu-id="ab25c-140">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ab25c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab25c-141">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ab25c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab25c-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab25c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab25c-143">INPUTOBJECT <IHealthBotIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="ab25c-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab25c-144">`[BotName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="ab25c-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="ab25c-145">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="ab25c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab25c-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ab25c-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="ab25c-147">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab25c-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ab25c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab25c-148">RELATED LINKS</span></span>

