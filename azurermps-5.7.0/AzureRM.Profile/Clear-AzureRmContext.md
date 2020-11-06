---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmContext.md
ms.openlocfilehash: 960e1b35a90b0bc1c490cbf194c20ac7a051e4d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508079"
---
# <span data-ttu-id="f3c89-101">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f3c89-101">Clear-AzureRmContext</span></span>

## <span data-ttu-id="f3c89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3c89-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c89-103">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c89-103">Remove all Azure credentials, account, and subscription information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3c89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3c89-104">SYNTAX</span></span>

```
Clear-AzureRmContext -Scope <ContextModificationScope> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c89-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3c89-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c89-106">Rimuovere tutte le informazioni sulle credenziali, l'account e l'abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="f3c89-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="f3c89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3c89-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c89-108">Cancellare un contesto globale</span><span class="sxs-lookup"><span data-stu-id="f3c89-108">Clear global context</span></span>
```
PS C:\> Clear-AzureRmContext -Scope CurrentUser
```

<span data-ttu-id="f3c89-109">Rimuovere tutte le informazioni sull'account, l'abbonamento e le credenziali per qualsiasi sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3c89-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="f3c89-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3c89-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c89-111">-DefaultProfile</span></span>
<span data-ttu-id="f3c89-112">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f3c89-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3c89-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f3c89-113">-Force</span></span>
<span data-ttu-id="f3c89-114">Eliminare tutti gli utenti e i gruppi dall'ambito globale senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="f3c89-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="f3c89-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3c89-115">-PassThru</span></span>
<span data-ttu-id="f3c89-116">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="f3c89-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="f3c89-117">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f3c89-117">-Scope</span></span>
<span data-ttu-id="f3c89-118">Deselezionare il contesto solo per la sessione di PowerShell corrente o per tutte le sessioni.</span><span class="sxs-lookup"><span data-stu-id="f3c89-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c89-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3c89-119">-Confirm</span></span>
<span data-ttu-id="f3c89-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3c89-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c89-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c89-121">-WhatIf</span></span>
<span data-ttu-id="f3c89-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3c89-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c89-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3c89-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c89-124">CommonParameters</span></span>
<span data-ttu-id="f3c89-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c89-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c89-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c89-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3c89-127">INPUTS</span></span>

### <span data-ttu-id="f3c89-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f3c89-128">None</span></span>

## <span data-ttu-id="f3c89-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3c89-129">OUTPUTS</span></span>

### <span data-ttu-id="f3c89-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c89-130">System.Boolean</span></span>
<span data-ttu-id="f3c89-131">True se il contesto è stato eliminato correttamente, false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f3c89-131">True if the context was successfully cleared, false otherwise.</span></span>

## <span data-ttu-id="f3c89-132">Note</span><span class="sxs-lookup"><span data-stu-id="f3c89-132">NOTES</span></span>

## <span data-ttu-id="f3c89-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3c89-133">RELATED LINKS</span></span>

