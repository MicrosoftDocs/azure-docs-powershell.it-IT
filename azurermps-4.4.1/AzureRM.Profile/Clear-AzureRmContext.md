---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 5a640bf705040c3bb8ed0f7dc985693b2e57c873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687999"
---
# <span data-ttu-id="2a0ef-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="2a0ef-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="2a0ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0ef-103">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a0ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a0ef-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a0ef-105">DESCRIPTION</span></span>
<span data-ttu-id="2a0ef-106">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="2a0ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a0ef-107">EXAMPLES</span></span>

### <span data-ttu-id="2a0ef-108">Cancellare un contesto globale</span><span class="sxs-lookup"><span data-stu-id="2a0ef-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="2a0ef-109">Rimuovere tutte le informazioni sull'account, l'abbonamento e le credenziali per qualsiasi sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="2a0ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a0ef-110">PARAMETERS</span></span>

### <span data-ttu-id="2a0ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0ef-111">-DefaultProfile</span></span>
<span data-ttu-id="2a0ef-112">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2a0ef-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a0ef-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2a0ef-113">-Force</span></span>
<span data-ttu-id="2a0ef-114">Eliminare tutti gli utenti e i gruppi dall'ambito globale senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="2a0ef-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="2a0ef-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a0ef-115">-PassThru</span></span>
<span data-ttu-id="2a0ef-116">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="2a0ef-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="2a0ef-117">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2a0ef-117">-Scope</span></span>
<span data-ttu-id="2a0ef-118">Deselezionare il contesto solo per la sessione di PowerShell corrente o per tutte le sessioni.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0ef-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a0ef-119">-Confirm</span></span>
<span data-ttu-id="2a0ef-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0ef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0ef-121">-WhatIf</span></span>
<span data-ttu-id="2a0ef-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0ef-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0ef-124">CommonParameters</span></span>
<span data-ttu-id="2a0ef-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0ef-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a0ef-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0ef-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a0ef-127">INPUTS</span></span>

### <span data-ttu-id="2a0ef-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2a0ef-128">None</span></span>

## <span data-ttu-id="2a0ef-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a0ef-129">OUTPUTS</span></span>

### <span data-ttu-id="2a0ef-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a0ef-130">System.Boolean</span></span>
<span data-ttu-id="2a0ef-131">True se il contesto è stato eliminato correttamente, false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2a0ef-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="2a0ef-132">Note</span><span class="sxs-lookup"><span data-stu-id="2a0ef-132">NOTES</span></span>

## <span data-ttu-id="2a0ef-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a0ef-133">RELATED LINKS</span></span>

