---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491170"
---
# <span data-ttu-id="6d98a-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6d98a-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="6d98a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d98a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d98a-103">Ottiene i metadati usati per autenticare le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d98a-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="6d98a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d98a-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="6d98a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d98a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d98a-106">Il cmdlet Get-AzureRmContext ottiene i metadati correnti usati per autenticare le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d98a-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="6d98a-107">Questo cmdlet consente di ottenere l'account di Active Directory, il tenant di Active Directory, l'abbonamento Azure e l'ambiente Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6d98a-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="6d98a-108">I cmdlet di Azure Resource Manager usano queste impostazioni per impostazione predefinita quando si effettuano richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d98a-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="6d98a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d98a-109">EXAMPLES</span></span>

### <span data-ttu-id="6d98a-110">Esempio 1: recupero del contesto corrente</span><span class="sxs-lookup"><span data-stu-id="6d98a-110">Example 1: Getting the current context</span></span>
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

<span data-ttu-id="6d98a-111">In questo esempio, stiamo accedendo al nostro account con un abbonamento a Azure usando Add-AzureRmAccount e quindi stiamo ottenendo il contesto della sessione corrente chiamando Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="6d98a-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="6d98a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d98a-112">PARAMETERS</span></span>

### <span data-ttu-id="6d98a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d98a-113">CommonParameters</span></span>
<span data-ttu-id="6d98a-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d98a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d98a-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d98a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d98a-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d98a-116">INPUTS</span></span>

## <span data-ttu-id="6d98a-117">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d98a-117">OUTPUTS</span></span>

### <span data-ttu-id="6d98a-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6d98a-118">PSAzureContext</span></span>
<span data-ttu-id="6d98a-119">Questo cmdlet restituisce l'account, il tenant e l'abbonamento usati dai cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="6d98a-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="6d98a-120">Note</span><span class="sxs-lookup"><span data-stu-id="6d98a-120">NOTES</span></span>

## <span data-ttu-id="6d98a-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d98a-121">RELATED LINKS</span></span>

[<span data-ttu-id="6d98a-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="6d98a-122">Set-AzureRMContext</span></span>]()

