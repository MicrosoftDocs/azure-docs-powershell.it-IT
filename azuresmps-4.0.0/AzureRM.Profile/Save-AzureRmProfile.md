---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06a78584437021df570bc5ff2b6ec19e332bffd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491321"
---
# <span data-ttu-id="e306c-101">Save-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="e306c-101">Save-AzureRmProfile</span></span>

## <span data-ttu-id="e306c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e306c-102">SYNOPSIS</span></span>
<span data-ttu-id="e306c-103">Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e306c-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="e306c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e306c-104">SYNTAX</span></span>

```
Save-AzureRmProfile [[-Profile] <AzureRMProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e306c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e306c-105">DESCRIPTION</span></span>
<span data-ttu-id="e306c-106">Il cmdlet Save-AzureRmProfile Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e306c-106">The Save-AzureRmProfile cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="e306c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e306c-107">EXAMPLES</span></span>

### <span data-ttu-id="e306c-108">Esempio 1: salvataggio del profilo della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="e306c-108">Example 1: Saving the current session's profile</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmProfile -Path C:\test.json
```

<span data-ttu-id="e306c-109">Questo esempio salva il profilo Azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="e306c-109">This example saves the current session's Azure profile to the JSON file provided.</span></span>

### <span data-ttu-id="e306c-110">Esempio 2: salvataggio di un profilo specifico</span><span class="sxs-lookup"><span data-stu-id="e306c-110">Example 2: Saving a given profile</span></span>
```
PS C:\> Save-AzureRmProfile -Profile (Add-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="e306c-111">Questo esempio salva il profilo Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="e306c-111">This example saves the Azure profile that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="e306c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e306c-112">PARAMETERS</span></span>

### <span data-ttu-id="e306c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e306c-113">-Force</span></span>
<span data-ttu-id="e306c-114">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="e306c-114">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="e306c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e306c-115">-Path</span></span>
<span data-ttu-id="e306c-116">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e306c-116">Specifies the path of the file to which to save authentication information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="e306c-117">-Profile</span></span>
<span data-ttu-id="e306c-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e306c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e306c-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e306c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e306c-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e306c-120">-Confirm</span></span>
<span data-ttu-id="e306c-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e306c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e306c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e306c-122">-WhatIf</span></span>
<span data-ttu-id="e306c-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e306c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e306c-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e306c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e306c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e306c-125">CommonParameters</span></span>
<span data-ttu-id="e306c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e306c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e306c-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e306c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e306c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e306c-128">INPUTS</span></span>

## <span data-ttu-id="e306c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e306c-129">OUTPUTS</span></span>

### <span data-ttu-id="e306c-130">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e306c-130">PSAzureProfile</span></span>

## <span data-ttu-id="e306c-131">Note</span><span class="sxs-lookup"><span data-stu-id="e306c-131">NOTES</span></span>

## <span data-ttu-id="e306c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e306c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e306c-133">Selezionare-AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="e306c-133">Select-AzureRMProfile</span></span>]()

