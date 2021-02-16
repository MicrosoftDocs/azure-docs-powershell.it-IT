---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178126"
---
# <span data-ttu-id="6b2c5-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="6b2c5-101">Get-AzContext</span></span>

## <span data-ttu-id="6b2c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2c5-103">Recupera i metadati usati per autenticare le richieste di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="6b2c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b2c5-104">SYNTAX</span></span>

### <span data-ttu-id="6b2c5-105">GetSingleContext (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b2c5-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b2c5-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="6b2c5-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b2c5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6b2c5-107">DESCRIPTION</span></span>
<span data-ttu-id="6b2c5-108">Il Get-AzContext cmdlet recupera i metadati correnti usati per autenticare le richieste di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="6b2c5-109">Questo cmdlet ottiene l'account di Active Directory, il tenant di Active Directory, la sottoscrizione di Azure e l'ambiente Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="6b2c5-110">I cmdlet di Gestione risorse di Azure usano queste impostazioni per impostazione predefinita quando effettuano richieste di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="6b2c5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b2c5-111">EXAMPLES</span></span>

### <span data-ttu-id="6b2c5-112">Esempio 1: Recupero del contesto corrente</span><span class="sxs-lookup"><span data-stu-id="6b2c5-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="6b2c5-113">In questo esempio si accede al proprio account con un abbonamento di Azure usando Connect-AzAccount e quindi si ottiene il contesto della sessione corrente chiamando Get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="6b2c5-114">Esempio 2: Elenco di tutti i contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="6b2c5-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="6b2c5-115">In questo esempio vengono visualizzati tutti i contesti attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="6b2c5-116">L'utente può selezionare uno di questi contesti usando Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="6b2c5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b2c5-117">PARAMETERS</span></span>

### <span data-ttu-id="6b2c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2c5-118">-DefaultProfile</span></span>
<span data-ttu-id="6b2c5-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6b2c5-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b2c5-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="6b2c5-120">-ListAvailable</span></span>
<span data-ttu-id="6b2c5-121">Elencare tutti i contesti disponibili nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="6b2c5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b2c5-122">-Name</span></span>
<span data-ttu-id="6b2c5-123">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="6b2c5-123">The name of the context</span></span>

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

### <span data-ttu-id="6b2c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2c5-124">CommonParameters</span></span>
<span data-ttu-id="6b2c5-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b2c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2c5-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2c5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2c5-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="6b2c5-127">INPUTS</span></span>

### <span data-ttu-id="6b2c5-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6b2c5-128">None</span></span>

## <span data-ttu-id="6b2c5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b2c5-129">OUTPUTS</span></span>

### <span data-ttu-id="6b2c5-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6b2c5-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6b2c5-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="6b2c5-131">NOTES</span></span>

## <span data-ttu-id="6b2c5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b2c5-132">RELATED LINKS</span></span>

[<span data-ttu-id="6b2c5-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="6b2c5-133">Set-AzContext</span></span>](./Set-AzContext.md)

