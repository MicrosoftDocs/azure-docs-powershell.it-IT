---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199762"
---
# <span data-ttu-id="96de2-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="96de2-101">Get-AzContext</span></span>

## <span data-ttu-id="96de2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96de2-102">SYNOPSIS</span></span>
<span data-ttu-id="96de2-103">Ottiene i metadati usati per autenticare le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="96de2-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="96de2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96de2-104">SYNTAX</span></span>

### <span data-ttu-id="96de2-105">GetSingleContext (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96de2-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="96de2-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="96de2-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96de2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96de2-107">DESCRIPTION</span></span>
<span data-ttu-id="96de2-108">Il cmdlet Get-AzContext ottiene i metadati correnti usati per autenticare le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="96de2-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="96de2-109">Questo cmdlet consente di ottenere l'account di Active Directory, il tenant di Active Directory, l'abbonamento Azure e l'ambiente Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="96de2-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="96de2-110">I cmdlet di Azure Resource Manager usano queste impostazioni per impostazione predefinita quando si effettuano richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="96de2-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="96de2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96de2-111">EXAMPLES</span></span>

### <span data-ttu-id="96de2-112">Esempio 1: recupero del contesto corrente</span><span class="sxs-lookup"><span data-stu-id="96de2-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="96de2-113">In questo esempio, stiamo accedendo al nostro account con un abbonamento a Azure usando Connect-AzAccount e quindi stiamo ottenendo il contesto della sessione corrente chiamando Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="96de2-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="96de2-114">Esempio 2: elenco di tutti i contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="96de2-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="96de2-115">In questo esempio vengono visualizzati tutti i contesti attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="96de2-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="96de2-116">L'utente può selezionare uno di questi contesti usando SELECT-AzContext.</span><span class="sxs-lookup"><span data-stu-id="96de2-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="96de2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96de2-117">PARAMETERS</span></span>

### <span data-ttu-id="96de2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96de2-118">-DefaultProfile</span></span>
<span data-ttu-id="96de2-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="96de2-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96de2-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="96de2-120">-ListAvailable</span></span>
<span data-ttu-id="96de2-121">Elencare tutti i contesti disponibili nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="96de2-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96de2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="96de2-122">-Name</span></span>
<span data-ttu-id="96de2-123">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="96de2-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96de2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96de2-124">CommonParameters</span></span>
<span data-ttu-id="96de2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96de2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96de2-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96de2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96de2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96de2-127">INPUTS</span></span>

### <span data-ttu-id="96de2-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96de2-128">None</span></span>

## <span data-ttu-id="96de2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96de2-129">OUTPUTS</span></span>

### <span data-ttu-id="96de2-130">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="96de2-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="96de2-131">Note</span><span class="sxs-lookup"><span data-stu-id="96de2-131">NOTES</span></span>

## <span data-ttu-id="96de2-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96de2-132">RELATED LINKS</span></span>

[<span data-ttu-id="96de2-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="96de2-133">Set-AzContext</span></span>](./Set-AzContext.md)
