---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479159"
---
# <span data-ttu-id="cb0d0-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="cb0d0-101">Get-AzSubscription</span></span>

## <span data-ttu-id="cb0d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb0d0-102">SYNOPSIS</span></span>
<span data-ttu-id="cb0d0-103">Ottenere gli abbonamenti a cui l'account corrente può accedere.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="cb0d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb0d0-104">SYNTAX</span></span>

### <span data-ttu-id="cb0d0-105">ListByIdInTenant (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb0d0-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb0d0-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="cb0d0-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb0d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb0d0-107">DESCRIPTION</span></span>
<span data-ttu-id="cb0d0-108">Il cmdlet Get-AzSubscription Ottiene l'ID sottoscrizione, il nome dell'abbonamento e il tenant Home per gli abbonamenti a cui l'account corrente può accedere.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="cb0d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb0d0-109">EXAMPLES</span></span>

### <span data-ttu-id="cb0d0-110">Esempio 1: ottenere tutte le sottoscrizioni in tutti i tenant</span><span class="sxs-lookup"><span data-stu-id="cb0d0-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="cb0d0-111">Questo comando consente di ottenere tutte le sottoscrizioni in tutti i tenant autorizzati per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="cb0d0-112">Esempio 2: ottenere tutti gli abbonamenti per un tenant specifico</span><span class="sxs-lookup"><span data-stu-id="cb0d0-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="cb0d0-113">Elencare tutte le sottoscrizioni nel tenant indicato autorizzato per l'account corrente.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="cb0d0-114">Esempio 3: ottenere tutte le sottoscrizioni nel tenant corrente</span><span class="sxs-lookup"><span data-stu-id="cb0d0-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="cb0d0-115">Questo comando consente di ottenere tutte le sottoscrizioni del tenant corrente autorizzate per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="cb0d0-116">Esempio 4: cambiare il contesto corrente in uso di un abbonamento specifico</span><span class="sxs-lookup"><span data-stu-id="cb0d0-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="cb0d0-117">Questo comando ottiene l'abbonamento specificato e quindi imposta il contesto corrente per usarlo.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="cb0d0-118">Tutti i cmdlet successivi in questa sessione usano il nuovo abbonamento (contoso Subscription 1) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="cb0d0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb0d0-119">PARAMETERS</span></span>

### <span data-ttu-id="cb0d0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb0d0-120">-AsJob</span></span>
<span data-ttu-id="cb0d0-121">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cb0d0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb0d0-122">-DefaultProfile</span></span>
<span data-ttu-id="cb0d0-123">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cb0d0-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb0d0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb0d0-124">-SubscriptionId</span></span>
<span data-ttu-id="cb0d0-125">Specifica l'ID della sottoscrizione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="cb0d0-126">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="cb0d0-126">-SubscriptionName</span></span>
<span data-ttu-id="cb0d0-127">Specifica il nome dell'abbonamento da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="cb0d0-128">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="cb0d0-128">-TenantId</span></span>
<span data-ttu-id="cb0d0-129">Specifica l'ID del tenant che contiene le sottoscrizioni da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="cb0d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb0d0-130">CommonParameters</span></span>
<span data-ttu-id="cb0d0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb0d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb0d0-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb0d0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb0d0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb0d0-133">INPUTS</span></span>

### <span data-ttu-id="cb0d0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cb0d0-134">System.String</span></span>

## <span data-ttu-id="cb0d0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb0d0-135">OUTPUTS</span></span>

### <span data-ttu-id="cb0d0-136">Microsoft. Azure. Commands. profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cb0d0-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="cb0d0-137">Note</span><span class="sxs-lookup"><span data-stu-id="cb0d0-137">NOTES</span></span>

## <span data-ttu-id="cb0d0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb0d0-138">RELATED LINKS</span></span>
