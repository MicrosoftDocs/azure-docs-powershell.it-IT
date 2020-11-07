---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/import-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Import-AzContext.md
ms.openlocfilehash: 145c5f65b00da7f143b04d526b8bcd959d323d12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676204"
---
# <span data-ttu-id="ca639-101">Import-AzContext</span><span class="sxs-lookup"><span data-stu-id="ca639-101">Import-AzContext</span></span>

## <span data-ttu-id="ca639-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca639-102">SYNOPSIS</span></span>
<span data-ttu-id="ca639-103">Carica le informazioni di autenticazione di Azure da un file.</span><span class="sxs-lookup"><span data-stu-id="ca639-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="ca639-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca639-104">SYNTAX</span></span>

### <span data-ttu-id="ca639-105">ProfileFromDisk (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca639-105">ProfileFromDisk (Default)</span></span>
```
Import-AzContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca639-106">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="ca639-106">InMemoryProfile</span></span>
```
Import-AzContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca639-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca639-107">DESCRIPTION</span></span>
<span data-ttu-id="ca639-108">Il cmdlet Import-AzContext carica le informazioni di autenticazione da un file per impostare l'ambiente e il contesto di Azure.</span><span class="sxs-lookup"><span data-stu-id="ca639-108">The Import-AzContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="ca639-109">I cmdlet eseguiti nella sessione corrente usano queste informazioni per autenticare le richieste in Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ca639-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="ca639-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca639-110">EXAMPLES</span></span>

### <span data-ttu-id="ca639-111">Esempio 1: importazione di un contesto da un AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ca639-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzContext -AzContext (Connect-AzAccount)

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ca639-112">Questo esempio importa un contesto da un PSAzureProfile passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca639-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="ca639-113">Esempio 2: importazione di un contesto da un file JSON</span><span class="sxs-lookup"><span data-stu-id="ca639-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzContext -Path C:\test.json

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="ca639-114">Questo esempio seleziona un contesto da un file JSON passato al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca639-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="ca639-115">Questo file JSON può essere creato da Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="ca639-115">This JSON file can be created from Save-AzContext.</span></span>

## <span data-ttu-id="ca639-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca639-116">PARAMETERS</span></span>

### <span data-ttu-id="ca639-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="ca639-117">-AzureContext</span></span>
<span data-ttu-id="ca639-118">{{Fill AzureContext Description}}</span><span class="sxs-lookup"><span data-stu-id="ca639-118">{{Fill AzureContext Description}}</span></span>

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

### <span data-ttu-id="ca639-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca639-119">-DefaultProfile</span></span>
<span data-ttu-id="ca639-120">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ca639-120">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca639-121">-Path</span><span class="sxs-lookup"><span data-stu-id="ca639-121">-Path</span></span>
<span data-ttu-id="ca639-122">Specifica il percorso delle informazioni sul contesto salvate tramite Save-AzContext.</span><span class="sxs-lookup"><span data-stu-id="ca639-122">Specifies the path to context information saved by using Save-AzContext.</span></span>

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

### <span data-ttu-id="ca639-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="ca639-123">-Scope</span></span>
<span data-ttu-id="ca639-124">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="ca639-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ca639-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca639-125">-Confirm</span></span>
<span data-ttu-id="ca639-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca639-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca639-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca639-127">-WhatIf</span></span>
<span data-ttu-id="ca639-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca639-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca639-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca639-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca639-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca639-130">CommonParameters</span></span>
<span data-ttu-id="ca639-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca639-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca639-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca639-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca639-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca639-133">INPUTS</span></span>

### <span data-ttu-id="ca639-134">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ca639-134">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

### <span data-ttu-id="ca639-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ca639-135">System.String</span></span>

## <span data-ttu-id="ca639-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca639-136">OUTPUTS</span></span>

### <span data-ttu-id="ca639-137">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ca639-137">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ca639-138">Note</span><span class="sxs-lookup"><span data-stu-id="ca639-138">NOTES</span></span>

## <span data-ttu-id="ca639-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca639-139">RELATED LINKS</span></span>
