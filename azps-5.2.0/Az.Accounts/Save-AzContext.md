---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331468"
---
# <span data-ttu-id="b3a8b-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="b3a8b-101">Save-AzContext</span></span>

## <span data-ttu-id="b3a8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a8b-103">Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="b3a8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3a8b-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3a8b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a8b-106">Il cmdlet Save-AzContext Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="b3a8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3a8b-107">EXAMPLES</span></span>

### <span data-ttu-id="b3a8b-108">Esempio 1: salvataggio del contesto della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="b3a8b-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="b3a8b-109">Questo esempio salva il contesto Azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="b3a8b-110">Esempio 2: salvataggio di un contesto specifico</span><span class="sxs-lookup"><span data-stu-id="b3a8b-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="b3a8b-111">Questo esempio salva il contesto Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="b3a8b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3a8b-112">PARAMETERS</span></span>

### <span data-ttu-id="b3a8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a8b-113">-DefaultProfile</span></span>
<span data-ttu-id="b3a8b-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3a8b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b3a8b-115">-Force</span></span>
<span data-ttu-id="b3a8b-116">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="b3a8b-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="b3a8b-117">-Path</span><span class="sxs-lookup"><span data-stu-id="b3a8b-117">-Path</span></span>
<span data-ttu-id="b3a8b-118">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-118">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a8b-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="b3a8b-119">-Profile</span></span>
<span data-ttu-id="b3a8b-120">Specifica il contesto Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="b3a8b-121">Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a8b-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3a8b-122">-Confirm</span></span>
<span data-ttu-id="b3a8b-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a8b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a8b-124">-WhatIf</span></span>
<span data-ttu-id="b3a8b-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a8b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a8b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a8b-127">CommonParameters</span></span>
<span data-ttu-id="b3a8b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a8b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a8b-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a8b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a8b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3a8b-130">INPUTS</span></span>

### <span data-ttu-id="b3a8b-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="b3a8b-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="b3a8b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3a8b-132">OUTPUTS</span></span>

### <span data-ttu-id="b3a8b-133">Microsoft. Azure. Commands. profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="b3a8b-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="b3a8b-134">Note</span><span class="sxs-lookup"><span data-stu-id="b3a8b-134">NOTES</span></span>

## <span data-ttu-id="b3a8b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3a8b-135">RELATED LINKS</span></span>
