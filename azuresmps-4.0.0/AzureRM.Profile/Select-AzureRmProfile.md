---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491325"
---
# <span data-ttu-id="c3e68-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="c3e68-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="c3e68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3e68-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e68-103">Carica le informazioni di autenticazione di Azure da un file.</span><span class="sxs-lookup"><span data-stu-id="c3e68-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="c3e68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3e68-104">SYNTAX</span></span>

### <span data-ttu-id="c3e68-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="c3e68-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="c3e68-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="c3e68-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="c3e68-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3e68-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e68-108">Il cmdlet Select-AzureRmProfile carica le informazioni di autenticazione da un file per impostare l'ambiente e il contesto di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e68-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="c3e68-109">I cmdlet eseguiti nella sessione corrente usano queste informazioni per autenticare le richieste in Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c3e68-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="c3e68-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3e68-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e68-111">Esempio 1: selezione di un profilo da un PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c3e68-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="c3e68-112">Questo esempio seleziona un profilo da un PSAzureProfile passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e68-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="c3e68-113">Esempio 2: selezione di un profilo da un file JSON</span><span class="sxs-lookup"><span data-stu-id="c3e68-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="c3e68-114">Questo esempio seleziona un profilo da un file JSON passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e68-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="c3e68-115">Questo file JSON può essere creato da Save-AzureRmProfile.</span><span class="sxs-lookup"><span data-stu-id="c3e68-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="c3e68-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3e68-116">PARAMETERS</span></span>

### <span data-ttu-id="c3e68-117">-Path</span><span class="sxs-lookup"><span data-stu-id="c3e68-117">-Path</span></span>
<span data-ttu-id="c3e68-118">Specifica il percorso delle informazioni del profilo salvate tramite Save-AzureRMProfile.</span><span class="sxs-lookup"><span data-stu-id="c3e68-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e68-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="c3e68-119">-Profile</span></span>
<span data-ttu-id="c3e68-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3e68-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c3e68-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c3e68-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e68-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e68-122">CommonParameters</span></span>
<span data-ttu-id="c3e68-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e68-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e68-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e68-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e68-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3e68-125">INPUTS</span></span>

## <span data-ttu-id="c3e68-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3e68-126">OUTPUTS</span></span>

### <span data-ttu-id="c3e68-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="c3e68-127">PSAzureProfile</span></span>

## <span data-ttu-id="c3e68-128">Note</span><span class="sxs-lookup"><span data-stu-id="c3e68-128">NOTES</span></span>

## <span data-ttu-id="c3e68-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3e68-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3e68-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="c3e68-130">Get-AzureRMContext</span></span>]()

