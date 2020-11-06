---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: cb232bdebacfcb65cf3570854b14c28406d22b12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519398"
---
# <span data-ttu-id="31301-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="31301-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="31301-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31301-102">SYNOPSIS</span></span>
<span data-ttu-id="31301-103">Rimuovere un contesto dal set di contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="31301-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31301-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31301-104">SYNTAX</span></span>

### <span data-ttu-id="31301-105">RemoveByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31301-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31301-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="31301-106">RemoveByName</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="31301-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31301-107">DESCRIPTION</span></span>
<span data-ttu-id="31301-108">Rimuovere un contesto Azure dal set di contesti</span><span class="sxs-lookup"><span data-stu-id="31301-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="31301-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31301-109">EXAMPLES</span></span>

### <span data-ttu-id="31301-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31301-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="31301-111">Rimuovere il contesto denominato default</span><span class="sxs-lookup"><span data-stu-id="31301-111">Remove the context named default</span></span>

## <span data-ttu-id="31301-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31301-112">PARAMETERS</span></span>

### <span data-ttu-id="31301-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31301-113">-DefaultProfile</span></span>
<span data-ttu-id="31301-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31301-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31301-115">-Force</span><span class="sxs-lookup"><span data-stu-id="31301-115">-Force</span></span>
<span data-ttu-id="31301-116">Rimuovi contesto anche se è il defualt</span><span class="sxs-lookup"><span data-stu-id="31301-116">Remove context even if it is the defualt</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31301-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31301-117">-InputObject</span></span>
<span data-ttu-id="31301-118">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="31301-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31301-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="31301-119">-Name</span></span>
<span data-ttu-id="31301-120">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="31301-120">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: RemoveByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31301-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31301-121">-PassThru</span></span>
<span data-ttu-id="31301-122">Restituire il contesto rimosso</span><span class="sxs-lookup"><span data-stu-id="31301-122">Return the removed context</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31301-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="31301-123">-Scope</span></span>
<span data-ttu-id="31301-124">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="31301-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="31301-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31301-125">-Confirm</span></span>
<span data-ttu-id="31301-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31301-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31301-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31301-127">-WhatIf</span></span>
<span data-ttu-id="31301-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31301-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31301-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31301-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31301-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31301-130">CommonParameters</span></span>
<span data-ttu-id="31301-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31301-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31301-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31301-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31301-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31301-133">INPUTS</span></span>

### <span data-ttu-id="31301-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31301-134">None</span></span>

## <span data-ttu-id="31301-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31301-135">OUTPUTS</span></span>

### <span data-ttu-id="31301-136">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="31301-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="31301-137">Note</span><span class="sxs-lookup"><span data-stu-id="31301-137">NOTES</span></span>

## <span data-ttu-id="31301-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31301-138">RELATED LINKS</span></span>

