---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 3ad029e84245aee45bbcdd08ea0d78c5e57b985e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516120"
---
# <span data-ttu-id="a81aa-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a81aa-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="a81aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a81aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a81aa-103">Ottiene i metadati usati per autenticare le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a81aa-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a81aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a81aa-104">SYNTAX</span></span>

### <span data-ttu-id="a81aa-105">GetSingleContext (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a81aa-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="a81aa-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="a81aa-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a81aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a81aa-107">DESCRIPTION</span></span>
<span data-ttu-id="a81aa-108">Il cmdlet Get-AzureRmContext ottiene i metadati correnti usati per autenticare le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a81aa-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="a81aa-109">Questo cmdlet consente di ottenere l'account di Active Directory, il tenant di Active Directory, l'abbonamento Azure e l'ambiente Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a81aa-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="a81aa-110">I cmdlet di Azure Resource Manager usano queste impostazioni per impostazione predefinita quando si effettuano richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="a81aa-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="a81aa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a81aa-111">EXAMPLES</span></span>

### <span data-ttu-id="a81aa-112">Esempio 1: recupero del contesto corrente</span><span class="sxs-lookup"><span data-stu-id="a81aa-112">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a81aa-113">In questo esempio, stiamo accedendo al nostro account con un abbonamento a Azure usando Add-AzureRmAccount e quindi stiamo ottenendo il contesto della sessione corrente chiamando Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="a81aa-113">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="a81aa-114">Esempio 2: elenco di tutti i contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="a81aa-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="a81aa-115">In questo esempio vengono visualizzati tutti i contesti attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="a81aa-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="a81aa-116">L'utente può selezionare uno di questi contesti usando SELECT-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="a81aa-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="a81aa-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a81aa-117">PARAMETERS</span></span>

### <span data-ttu-id="a81aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a81aa-118">-DefaultProfile</span></span>
<span data-ttu-id="a81aa-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a81aa-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81aa-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="a81aa-120">-ListAvailable</span></span>
<span data-ttu-id="a81aa-121">Elencare tutti i contesti disponibili nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="a81aa-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="a81aa-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a81aa-122">-Name</span></span>
<span data-ttu-id="a81aa-123">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="a81aa-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a81aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a81aa-124">CommonParameters</span></span>
<span data-ttu-id="a81aa-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a81aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a81aa-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a81aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a81aa-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a81aa-127">INPUTS</span></span>

## <span data-ttu-id="a81aa-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a81aa-128">OUTPUTS</span></span>

### <span data-ttu-id="a81aa-129">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a81aa-129">PSAzureContext</span></span>
<span data-ttu-id="a81aa-130">Questo cmdlet restituisce l'account, il tenant e l'abbonamento usati dai cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a81aa-130">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="a81aa-131">Note</span><span class="sxs-lookup"><span data-stu-id="a81aa-131">NOTES</span></span>

## <span data-ttu-id="a81aa-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a81aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="a81aa-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="a81aa-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

