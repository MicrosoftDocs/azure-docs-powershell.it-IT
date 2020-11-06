---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: 451498760d85cc018b8fbade625625ec6ecc1910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511575"
---
# <span data-ttu-id="91c84-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="91c84-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="91c84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91c84-102">SYNOPSIS</span></span>
<span data-ttu-id="91c84-103">Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91c84-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91c84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91c84-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91c84-105">DESCRIPTION</span></span>
<span data-ttu-id="91c84-106">Il cmdlet Save-AzureRmContext Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91c84-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="91c84-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91c84-107">EXAMPLES</span></span>

### <span data-ttu-id="91c84-108">Esempio 1: salvataggio del contesto della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="91c84-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="91c84-109">Questo esempio salva il contesto Azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="91c84-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="91c84-110">Esempio 2: salvataggio di un contesto specifico</span><span class="sxs-lookup"><span data-stu-id="91c84-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="91c84-111">Questo esempio salva il contesto Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="91c84-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="91c84-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91c84-112">PARAMETERS</span></span>

### <span data-ttu-id="91c84-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c84-113">-DefaultProfile</span></span>
<span data-ttu-id="91c84-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91c84-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c84-115">-Force</span><span class="sxs-lookup"><span data-stu-id="91c84-115">-Force</span></span>
<span data-ttu-id="91c84-116">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="91c84-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="91c84-117">-Path</span><span class="sxs-lookup"><span data-stu-id="91c84-117">-Path</span></span>
<span data-ttu-id="91c84-118">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="91c84-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="91c84-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="91c84-119">-Profile</span></span>
<span data-ttu-id="91c84-120">Specifica il contesto Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c84-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="91c84-121">Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="91c84-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="91c84-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91c84-122">-Confirm</span></span>
<span data-ttu-id="91c84-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c84-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c84-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c84-124">-WhatIf</span></span>
<span data-ttu-id="91c84-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91c84-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c84-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91c84-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c84-127">CommonParameters</span></span>
<span data-ttu-id="91c84-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c84-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c84-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c84-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91c84-130">INPUTS</span></span>

### <span data-ttu-id="91c84-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="91c84-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile</span></span>
<span data-ttu-id="91c84-132">Parametri: profile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91c84-132">Parameters: Profile (ByValue)</span></span>

## <span data-ttu-id="91c84-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91c84-133">OUTPUTS</span></span>

### <span data-ttu-id="91c84-134">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="91c84-134">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="91c84-135">Note</span><span class="sxs-lookup"><span data-stu-id="91c84-135">NOTES</span></span>

## <span data-ttu-id="91c84-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91c84-136">RELATED LINKS</span></span>
