---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490453"
---
# <span data-ttu-id="63d1f-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="63d1f-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="63d1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="63d1f-103">Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63d1f-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="63d1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63d1f-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="63d1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63d1f-105">DESCRIPTION</span></span>
<span data-ttu-id="63d1f-106">Il cmdlet Save-AzureRmContext Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="63d1f-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="63d1f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63d1f-107">EXAMPLES</span></span>

### <span data-ttu-id="63d1f-108">Esempio 1: salvataggio del contesto della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="63d1f-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="63d1f-109">Questo esempio salva il contesto Azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="63d1f-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="63d1f-110">Esempio 2: salvataggio di un contesto specifico</span><span class="sxs-lookup"><span data-stu-id="63d1f-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="63d1f-111">Questo esempio salva il contesto Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="63d1f-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="63d1f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63d1f-112">PARAMETERS</span></span>

### <span data-ttu-id="63d1f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="63d1f-113">-Force</span></span>
<span data-ttu-id="63d1f-114">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="63d1f-114">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d1f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="63d1f-115">-Path</span></span>
<span data-ttu-id="63d1f-116">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="63d1f-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d1f-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="63d1f-117">-Profile</span></span>
<span data-ttu-id="63d1f-118">Specifica il contesto Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d1f-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="63d1f-119">Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="63d1f-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63d1f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="63d1f-120">-Confirm</span></span>
<span data-ttu-id="63d1f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d1f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d1f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d1f-122">-WhatIf</span></span>
<span data-ttu-id="63d1f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63d1f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63d1f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="63d1f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="63d1f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63d1f-125">INPUTS</span></span>

### <span data-ttu-id="63d1f-126">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="63d1f-126">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="63d1f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63d1f-127">OUTPUTS</span></span>

### <span data-ttu-id="63d1f-128">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="63d1f-128">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="63d1f-129">Note</span><span class="sxs-lookup"><span data-stu-id="63d1f-129">NOTES</span></span>

## <span data-ttu-id="63d1f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63d1f-130">RELATED LINKS</span></span>

