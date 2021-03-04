---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: f2d080373bef1abda3ea5af91076b024261d3eeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955038"
---
# <span data-ttu-id="308f6-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="308f6-101">Get-AzSubscription</span></span>

## <span data-ttu-id="308f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="308f6-102">SYNOPSIS</span></span>
<span data-ttu-id="308f6-103">Ottenere abbonamenti a cui può accedere l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="308f6-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="308f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="308f6-104">SYNTAX</span></span>

### <span data-ttu-id="308f6-105">ListByIdInTenant (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="308f6-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="308f6-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="308f6-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="308f6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="308f6-107">DESCRIPTION</span></span>
<span data-ttu-id="308f6-108">Il cmdlet Get-AzSubscription cmdlet ottiene l'ID dell'abbonamento, il nome dell'abbonamento e il tenant home per le sottoscrizioni a cui può accedere l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="308f6-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="308f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="308f6-109">EXAMPLES</span></span>

### <span data-ttu-id="308f6-110">Esempio 1: Ottenere tutti gli abbonamenti in tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="308f6-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="308f6-111">Questo comando recupera tutte le sottoscrizioni in tutti i tenant autorizzati per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="308f6-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="308f6-112">Esempio 2: Ottenere tutte le sottoscrizioni per un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="308f6-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="308f6-113">Elencare tutte le sottoscrizioni del tenant specificato autorizzate per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="308f6-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="308f6-114">Esempio 3: Ottenere tutti gli abbonamenti nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="308f6-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="308f6-115">Questo comando recupera tutte le sottoscrizioni nel tenant corrente autorizzate per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="308f6-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="308f6-116">Esempio 4: Modificare il contesto corrente per usare una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="308f6-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="308f6-117">Questo comando ottiene la sottoscrizione specificata e quindi imposta il contesto corrente per usarlo.</span><span class="sxs-lookup"><span data-stu-id="308f6-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="308f6-118">Tutti i cmdlet successivi in questa sessione usano il nuovo abbonamento (Abbonamento Contoso 1) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="308f6-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="308f6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="308f6-119">PARAMETERS</span></span>

### <span data-ttu-id="308f6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="308f6-120">-AsJob</span></span>
<span data-ttu-id="308f6-121">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="308f6-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="308f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="308f6-122">-DefaultProfile</span></span>
<span data-ttu-id="308f6-123">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="308f6-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="308f6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="308f6-124">-SubscriptionId</span></span>
<span data-ttu-id="308f6-125">Specifica l'ID della sottoscrizione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="308f6-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308f6-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="308f6-126">-SubscriptionName</span></span>
<span data-ttu-id="308f6-127">Specifica il nome dell'abbonamento da ottenere.</span><span class="sxs-lookup"><span data-stu-id="308f6-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308f6-128">-TenantId</span><span class="sxs-lookup"><span data-stu-id="308f6-128">-TenantId</span></span>
<span data-ttu-id="308f6-129">Specifica l'ID del tenant che contiene le sottoscrizioni da ottenere.</span><span class="sxs-lookup"><span data-stu-id="308f6-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="308f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="308f6-130">CommonParameters</span></span>
<span data-ttu-id="308f6-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="308f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="308f6-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="308f6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="308f6-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="308f6-133">INPUTS</span></span>

### <span data-ttu-id="308f6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="308f6-134">System.String</span></span>

## <span data-ttu-id="308f6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="308f6-135">OUTPUTS</span></span>

### <span data-ttu-id="308f6-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="308f6-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="308f6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="308f6-137">NOTES</span></span>

## <span data-ttu-id="308f6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="308f6-138">RELATED LINKS</span></span>
