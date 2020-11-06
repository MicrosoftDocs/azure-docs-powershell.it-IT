---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/select-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Select-AzureRmContext.md
ms.openlocfilehash: c002db2d04905c19c3229a45feb9e00b5dc15754
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520423"
---
# <span data-ttu-id="f0d9c-101">Select-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f0d9c-101">Select-AzureRmContext</span></span>

## <span data-ttu-id="f0d9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d9c-103">Selezionare un abbonamento e un account per la destinazione nei cmdlet di PowerShell di Azure</span><span class="sxs-lookup"><span data-stu-id="f0d9c-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0d9c-104">SYNTAX</span></span>

### <span data-ttu-id="f0d9c-105">SelectByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0d9c-105">SelectByInputObject (Default)</span></span>
```
Select-AzureRmContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d9c-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="f0d9c-106">SelectByName</span></span>
```
Select-AzureRmContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="f0d9c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="f0d9c-108">Selezionare un abbonamento a destinazione (o account o tenant) nei cmdlet di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="f0d9c-109">Dopo questo cmdlet, i futuri cmdlet verranno destinati al contesto selezionato.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="f0d9c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0d9c-110">EXAMPLES</span></span>

### <span data-ttu-id="f0d9c-111">Esempio 1: destinazione di un contesto denominato</span><span class="sxs-lookup"><span data-stu-id="f0d9c-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzureRmContext "Work"
```

<span data-ttu-id="f0d9c-112">I futuri cmdlet di PowerShell di Azure di destinazione per l'account, il tenant e l'abbonamento nel contesto "lavoro".</span><span class="sxs-lookup"><span data-stu-id="f0d9c-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="f0d9c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0d9c-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d9c-114">-DefaultProfile</span></span>
<span data-ttu-id="f0d9c-115">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0d9c-115">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d9c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0d9c-116">-InputObject</span></span>
<span data-ttu-id="f0d9c-117">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: SelectByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d9c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f0d9c-118">-Name</span></span>
<span data-ttu-id="f0d9c-119">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="f0d9c-119">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: SelectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d9c-120">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f0d9c-120">-Scope</span></span>
<span data-ttu-id="f0d9c-121">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="f0d9c-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d9c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f0d9c-122">-Confirm</span></span>
<span data-ttu-id="f0d9c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d9c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d9c-124">-WhatIf</span></span>
<span data-ttu-id="f0d9c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d9c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d9c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d9c-127">CommonParameters</span></span>
<span data-ttu-id="f0d9c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d9c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d9c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d9c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d9c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0d9c-130">INPUTS</span></span>

### <span data-ttu-id="f0d9c-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f0d9c-131">None</span></span>

## <span data-ttu-id="f0d9c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0d9c-132">OUTPUTS</span></span>

### <span data-ttu-id="f0d9c-133">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f0d9c-133">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="f0d9c-134">Note</span><span class="sxs-lookup"><span data-stu-id="f0d9c-134">NOTES</span></span>

## <span data-ttu-id="f0d9c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0d9c-135">RELATED LINKS</span></span>

