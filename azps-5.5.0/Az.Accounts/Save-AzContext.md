---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: 2d3506fcf0968e58a71d81fbabe56f08428af761
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176575"
---
# <span data-ttu-id="38cb8-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="38cb8-101">Save-AzContext</span></span>

## <span data-ttu-id="38cb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="38cb8-103">Salva le informazioni di autenticazione correnti per l'uso in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38cb8-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="38cb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38cb8-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38cb8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="38cb8-106">Il Save-AzContext cmdlet salva le informazioni di autenticazione correnti per l'uso in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="38cb8-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="38cb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="38cb8-108">Esempio 1: Salvataggio del contesto della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="38cb8-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="38cb8-109">Questo esempio salva il contesto Azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="38cb8-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="38cb8-110">Esempio 2: Salvataggio di un determinato contesto</span><span class="sxs-lookup"><span data-stu-id="38cb8-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="38cb8-111">Questo esempio salva il contesto di Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="38cb8-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="38cb8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38cb8-112">PARAMETERS</span></span>

### <span data-ttu-id="38cb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38cb8-113">-DefaultProfile</span></span>
<span data-ttu-id="38cb8-114">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38cb8-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38cb8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="38cb8-115">-Force</span></span>
<span data-ttu-id="38cb8-116">Sovrascrivere il file specificato, se esistente</span><span class="sxs-lookup"><span data-stu-id="38cb8-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="38cb8-117">-Path</span><span class="sxs-lookup"><span data-stu-id="38cb8-117">-Path</span></span>
<span data-ttu-id="38cb8-118">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="38cb8-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="38cb8-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="38cb8-119">-Profile</span></span>
<span data-ttu-id="38cb8-120">Specifica il contesto di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cb8-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="38cb8-121">Se non si specifica un contesto, questo cmdlet legge dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="38cb8-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="38cb8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38cb8-122">-Confirm</span></span>
<span data-ttu-id="38cb8-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38cb8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38cb8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38cb8-124">-WhatIf</span></span>
<span data-ttu-id="38cb8-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38cb8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38cb8-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38cb8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38cb8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38cb8-127">CommonParameters</span></span>
<span data-ttu-id="38cb8-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38cb8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38cb8-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38cb8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38cb8-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="38cb8-130">INPUTS</span></span>

### <span data-ttu-id="38cb8-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="38cb8-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="38cb8-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38cb8-132">OUTPUTS</span></span>

### <span data-ttu-id="38cb8-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="38cb8-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="38cb8-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="38cb8-134">NOTES</span></span>

## <span data-ttu-id="38cb8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38cb8-135">RELATED LINKS</span></span>
