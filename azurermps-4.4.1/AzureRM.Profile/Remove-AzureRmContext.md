---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 8bc129ddc1b4291ea7b3c9100a964bf5bb1dcee6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521567"
---
# <span data-ttu-id="58644-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="58644-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="58644-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58644-102">SYNOPSIS</span></span>
<span data-ttu-id="58644-103">Rimuovere un contesto dal set di contesti disponibili</span><span class="sxs-lookup"><span data-stu-id="58644-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58644-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58644-104">SYNTAX</span></span>

### <span data-ttu-id="58644-105">Oggetto di input (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58644-105">Input Object (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58644-106">Contesto denominato</span><span class="sxs-lookup"><span data-stu-id="58644-106">Named Context</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="58644-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58644-107">DESCRIPTION</span></span>
<span data-ttu-id="58644-108">Rimuovere un contesto Azure dal set di contesti</span><span class="sxs-lookup"><span data-stu-id="58644-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="58644-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58644-109">EXAMPLES</span></span>

### <span data-ttu-id="58644-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58644-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="58644-111">Rimuovere il contesto denominato default</span><span class="sxs-lookup"><span data-stu-id="58644-111">Remove the context named default</span></span>

## <span data-ttu-id="58644-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58644-112">PARAMETERS</span></span>

### <span data-ttu-id="58644-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58644-113">-DefaultProfile</span></span>
<span data-ttu-id="58644-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58644-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58644-115">-Force</span><span class="sxs-lookup"><span data-stu-id="58644-115">-Force</span></span>
<span data-ttu-id="58644-116">Rimuovi contesto anche se è il defualt</span><span class="sxs-lookup"><span data-stu-id="58644-116">Remove context even if it is the defualt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58644-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58644-117">-InputObject</span></span>
<span data-ttu-id="58644-118">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="58644-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="58644-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="58644-119">-Name</span></span>
<span data-ttu-id="58644-120">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="58644-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Named Context
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58644-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58644-121">-PassThru</span></span>
<span data-ttu-id="58644-122">Restituire il contesto rimosso</span><span class="sxs-lookup"><span data-stu-id="58644-122">Return the removed context</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58644-123">-Ambito</span><span class="sxs-lookup"><span data-stu-id="58644-123">-Scope</span></span>
<span data-ttu-id="58644-124">Determina l'ambito delle modifiche al contesto, ad esempio le modifiche apportate a wheher si applicano solo al processo cusrrent o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="58644-124">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="58644-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58644-125">-Confirm</span></span>
<span data-ttu-id="58644-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58644-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58644-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58644-127">-WhatIf</span></span>
<span data-ttu-id="58644-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58644-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58644-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58644-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58644-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58644-130">CommonParameters</span></span>
<span data-ttu-id="58644-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58644-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58644-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58644-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58644-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58644-133">INPUTS</span></span>

### <span data-ttu-id="58644-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58644-134">None</span></span>

## <span data-ttu-id="58644-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58644-135">OUTPUTS</span></span>

### <span data-ttu-id="58644-136">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="58644-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="58644-137">Note</span><span class="sxs-lookup"><span data-stu-id="58644-137">NOTES</span></span>

## <span data-ttu-id="58644-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58644-138">RELATED LINKS</span></span>

