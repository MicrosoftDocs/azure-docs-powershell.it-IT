---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516111"
---
# <span data-ttu-id="3bf21-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="3bf21-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="3bf21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bf21-102">SYNOPSIS</span></span>
<span data-ttu-id="3bf21-103">Carica le informazioni di autenticazione di Azure da un file.</span><span class="sxs-lookup"><span data-stu-id="3bf21-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bf21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bf21-104">SYNTAX</span></span>

### <span data-ttu-id="3bf21-105">ProfileFromDisk (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3bf21-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bf21-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="3bf21-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bf21-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bf21-107">DESCRIPTION</span></span>
<span data-ttu-id="3bf21-108">Il cmdlet Import-AzureRmContext carica le informazioni di autenticazione da un file per impostare l'ambiente e il contesto di Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf21-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="3bf21-109">I cmdlet eseguiti nella sessione corrente usano queste informazioni per autenticare le richieste in Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3bf21-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="3bf21-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bf21-110">EXAMPLES</span></span>

### <span data-ttu-id="3bf21-111">Esempio 1: importazione di un contesto da un AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="3bf21-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3bf21-112">Questo esempio importa un contesto da un PSAzureProfile passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bf21-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="3bf21-113">Esempio 2: importazione di un contesto da un file JSON</span><span class="sxs-lookup"><span data-stu-id="3bf21-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="3bf21-114">Questo esempio seleziona un contesto da un file JSON passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bf21-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="3bf21-115">Questo file JSON può essere creato da Save-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="3bf21-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="3bf21-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bf21-116">PARAMETERS</span></span>

### <span data-ttu-id="3bf21-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="3bf21-117">-AzureContext</span></span>
<span data-ttu-id="3bf21-118">Specifica il contesto Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bf21-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="3bf21-119">Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3bf21-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf21-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bf21-120">-DefaultProfile</span></span>
<span data-ttu-id="3bf21-121">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3bf21-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bf21-122">-Path</span><span class="sxs-lookup"><span data-stu-id="3bf21-122">-Path</span></span>
<span data-ttu-id="3bf21-123">Specifica il percorso delle informazioni sul contesto salvate tramite Save-AzureRMContext.</span><span class="sxs-lookup"><span data-stu-id="3bf21-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bf21-124">-Ambito</span><span class="sxs-lookup"><span data-stu-id="3bf21-124">-Scope</span></span>
<span data-ttu-id="3bf21-125">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="3bf21-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf21-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3bf21-126">-Confirm</span></span>
<span data-ttu-id="3bf21-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bf21-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf21-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bf21-128">-WhatIf</span></span>
<span data-ttu-id="3bf21-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bf21-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bf21-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bf21-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bf21-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bf21-131">CommonParameters</span></span>
<span data-ttu-id="3bf21-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bf21-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bf21-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bf21-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bf21-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bf21-134">INPUTS</span></span>

### <span data-ttu-id="3bf21-135">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="3bf21-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="3bf21-136">Contiene il set di credenziali, account e abbonamenti usati per comunicare con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf21-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="3bf21-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bf21-137">OUTPUTS</span></span>

### <span data-ttu-id="3bf21-138">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3bf21-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="3bf21-139">Contiene il set di credenziali, account e abbonamenti che possono essere usati per comunicare con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bf21-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="3bf21-140">Note</span><span class="sxs-lookup"><span data-stu-id="3bf21-140">NOTES</span></span>

## <span data-ttu-id="3bf21-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bf21-141">RELATED LINKS</span></span>

