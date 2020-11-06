---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490450"
---
# <span data-ttu-id="3b703-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3b703-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="3b703-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b703-102">SYNOPSIS</span></span>
<span data-ttu-id="3b703-103">Carica le informazioni di autenticazione di Azure da un file.</span><span class="sxs-lookup"><span data-stu-id="3b703-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="3b703-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b703-104">SYNTAX</span></span>

### <span data-ttu-id="3b703-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="3b703-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3b703-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="3b703-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3b703-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b703-107">DESCRIPTION</span></span>
<span data-ttu-id="3b703-108">Il cmdlet Import-AzureRmContext carica le informazioni di autenticazione da un file per impostare l'ambiente e il contesto di Azure.</span><span class="sxs-lookup"><span data-stu-id="3b703-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="3b703-109">I cmdlet eseguiti nella sessione corrente usano queste informazioni per autenticare le richieste in Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3b703-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="3b703-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b703-110">EXAMPLES</span></span>

### <span data-ttu-id="3b703-111">Esempio 1: importazione di un contesto da un AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="3b703-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3b703-112">Questo esempio importa un contesto da un PSAzureProfile passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b703-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="3b703-113">Esempio 2: importazione di un contesto da un file JSON</span><span class="sxs-lookup"><span data-stu-id="3b703-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3b703-114">Questo esempio seleziona un contesto da un file JSON passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b703-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="3b703-115">Questo file JSON può essere creato da Import-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="3b703-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="3b703-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b703-116">PARAMETERS</span></span>

### <span data-ttu-id="3b703-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="3b703-117">-AzureContext</span></span>
<span data-ttu-id="3b703-118">Specifica il contesto Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b703-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="3b703-119">Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3b703-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b703-120">-Path</span><span class="sxs-lookup"><span data-stu-id="3b703-120">-Path</span></span>
<span data-ttu-id="3b703-121">Specifica il percorso delle informazioni sul contesto salvate tramite Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="3b703-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b703-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b703-122">-Confirm</span></span>
<span data-ttu-id="3b703-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b703-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b703-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b703-124">-WhatIf</span></span>
<span data-ttu-id="3b703-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b703-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b703-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b703-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="3b703-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b703-127">INPUTS</span></span>

### <span data-ttu-id="3b703-128">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="3b703-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="3b703-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3b703-129">System.String</span></span>

## <span data-ttu-id="3b703-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b703-130">OUTPUTS</span></span>

### <span data-ttu-id="3b703-131">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3b703-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="3b703-132">Note</span><span class="sxs-lookup"><span data-stu-id="3b703-132">NOTES</span></span>

## <span data-ttu-id="3b703-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b703-133">RELATED LINKS</span></span>

