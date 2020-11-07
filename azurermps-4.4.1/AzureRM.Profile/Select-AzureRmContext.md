---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: 5450939ba5d0dc2fb1ae6c475d51b6fc9187082c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686806"
---
# <span data-ttu-id="1fe14-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="1fe14-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="1fe14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fe14-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe14-103">Selezionare un abbonamento e un account per la destinazione nei cmdlet di PowerShell di Azure</span><span class="sxs-lookup"><span data-stu-id="1fe14-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fe14-104">SYNTAX</span></span>

### <span data-ttu-id="1fe14-105">Oggetto di input (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1fe14-105">Input Object (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe14-106">Nome contesto</span><span class="sxs-lookup"><span data-stu-id="1fe14-106">Context Name</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="1fe14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe14-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe14-108">Selezionare un abbonamento a destinazione (o account o tenant) nei cmdlet di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe14-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="1fe14-109">Dopo questo cmdlet, i futuri cmdlet verranno destinati al contesto selezionato.</span><span class="sxs-lookup"><span data-stu-id="1fe14-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="1fe14-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fe14-110">EXAMPLES</span></span>

### <span data-ttu-id="1fe14-111">Esempio 1: destinazione di un contesto denominato</span><span class="sxs-lookup"><span data-stu-id="1fe14-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="1fe14-112">I futuri cmdlet di PowerShell di Azure di destinazione per l'account, il tenant e l'abbonamento nel contesto "lavoro".</span><span class="sxs-lookup"><span data-stu-id="1fe14-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="1fe14-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fe14-113">PARAMETERS</span></span>

### <span data-ttu-id="1fe14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe14-114">-DefaultProfile</span></span>
<span data-ttu-id="1fe14-115">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1fe14-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fe14-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe14-116">-InputObject</span></span>
<span data-ttu-id="1fe14-117">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1fe14-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe14-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fe14-118">-Name</span></span>
<span data-ttu-id="1fe14-119">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="1fe14-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe14-120">-Ambito</span><span class="sxs-lookup"><span data-stu-id="1fe14-120">-Scope</span></span>
<span data-ttu-id="1fe14-121">Determina l'ambito delle modifiche al contesto, ad esempio le modifiche apportate a wheher si applicano solo al processo cusrrent o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="1fe14-121">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="1fe14-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fe14-122">-Confirm</span></span>
<span data-ttu-id="1fe14-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe14-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe14-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe14-124">-WhatIf</span></span>
<span data-ttu-id="1fe14-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fe14-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe14-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fe14-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe14-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe14-127">CommonParameters</span></span>
<span data-ttu-id="1fe14-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe14-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe14-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe14-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe14-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fe14-130">INPUTS</span></span>

### <span data-ttu-id="1fe14-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1fe14-131">None</span></span>

## <span data-ttu-id="1fe14-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fe14-132">OUTPUTS</span></span>

### <span data-ttu-id="1fe14-133">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="1fe14-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="1fe14-134">Note</span><span class="sxs-lookup"><span data-stu-id="1fe14-134">NOTES</span></span>

## <span data-ttu-id="1fe14-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fe14-135">RELATED LINKS</span></span>

