---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/save-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Save-AzContext.md
ms.openlocfilehash: f73ca19ffa2c68599a5244d41b39d90ebbd2835a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975661"
---
# <span data-ttu-id="ffaef-101">Save-AzContext</span><span class="sxs-lookup"><span data-stu-id="ffaef-101">Save-AzContext</span></span>

## <span data-ttu-id="ffaef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffaef-102">SYNOPSIS</span></span>
<span data-ttu-id="ffaef-103">Salva le informazioni di autenticazione correnti per l'uso in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ffaef-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ffaef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffaef-104">SYNTAX</span></span>

```
Save-AzContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffaef-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ffaef-105">DESCRIPTION</span></span>
<span data-ttu-id="ffaef-106">Il Save-AzContext di autenticazione corrente salva le informazioni di autenticazione correnti per l'uso in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ffaef-106">The Save-AzContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="ffaef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffaef-107">EXAMPLES</span></span>

### <span data-ttu-id="ffaef-108">Esempio 1: Salvataggio del contesto della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="ffaef-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Save-AzContext -Path C:\test.json
```

<span data-ttu-id="ffaef-109">Questo esempio salva il contesto azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="ffaef-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="ffaef-110">Esempio 2: Salvataggio di un determinato contesto</span><span class="sxs-lookup"><span data-stu-id="ffaef-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzContext -Profile (Connect-AzAccount) -Path C:\test.json
```

<span data-ttu-id="ffaef-111">Questo esempio salva il contesto di Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="ffaef-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="ffaef-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffaef-112">PARAMETERS</span></span>

### <span data-ttu-id="ffaef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffaef-113">-DefaultProfile</span></span>
<span data-ttu-id="ffaef-114">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffaef-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffaef-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ffaef-115">-Force</span></span>
<span data-ttu-id="ffaef-116">Sovrascrivere il file specificato, se esistente</span><span class="sxs-lookup"><span data-stu-id="ffaef-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ffaef-117">-Path</span><span class="sxs-lookup"><span data-stu-id="ffaef-117">-Path</span></span>
<span data-ttu-id="ffaef-118">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ffaef-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="ffaef-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="ffaef-119">-Profile</span></span>
<span data-ttu-id="ffaef-120">Specifica il contesto di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffaef-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="ffaef-121">Se non si specifica un contesto, questo cmdlet legge dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ffaef-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="ffaef-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffaef-122">-Confirm</span></span>
<span data-ttu-id="ffaef-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffaef-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffaef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffaef-124">-WhatIf</span></span>
<span data-ttu-id="ffaef-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffaef-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffaef-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffaef-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffaef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffaef-127">CommonParameters</span></span>
<span data-ttu-id="ffaef-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffaef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffaef-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffaef-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffaef-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="ffaef-130">INPUTS</span></span>

### <span data-ttu-id="ffaef-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ffaef-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>

## <span data-ttu-id="ffaef-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffaef-132">OUTPUTS</span></span>

### <span data-ttu-id="ffaef-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ffaef-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="ffaef-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="ffaef-134">NOTES</span></span>

## <span data-ttu-id="ffaef-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffaef-135">RELATED LINKS</span></span>
