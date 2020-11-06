---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/save-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Save-AzureRmContext.md
ms.openlocfilehash: c605921d56cb9fd70005c290d696e5f50b0d4175
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519395"
---
# <span data-ttu-id="d321a-101">Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="d321a-101">Save-AzureRmContext</span></span>

## <span data-ttu-id="d321a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d321a-102">SYNOPSIS</span></span>
<span data-ttu-id="d321a-103">Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d321a-103">Saves the current authentication information for use in other PowerShell sessions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d321a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d321a-104">SYNTAX</span></span>

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d321a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d321a-105">DESCRIPTION</span></span>
<span data-ttu-id="d321a-106">Il cmdlet Save-AzureRmContext Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d321a-106">The Save-AzureRmContext cmdlet saves the current authentication information for use in other PowerShell sessions.</span></span>

## <span data-ttu-id="d321a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d321a-107">EXAMPLES</span></span>

### <span data-ttu-id="d321a-108">Esempio 1: salvataggio del contesto della sessione corrente</span><span class="sxs-lookup"><span data-stu-id="d321a-108">Example 1: Saving the current session's context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

<span data-ttu-id="d321a-109">Questo esempio salva il contesto Azure della sessione corrente nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="d321a-109">This example saves the current session's Azure context to the JSON file provided.</span></span>

### <span data-ttu-id="d321a-110">Esempio 2: salvataggio di un contesto specifico</span><span class="sxs-lookup"><span data-stu-id="d321a-110">Example 2: Saving a given context</span></span>
```
PS C:\> Save-AzureRmContext -Profile (Connect-AzureRmAccount) -Path C:\test.json
```

<span data-ttu-id="d321a-111">Questo esempio salva il contesto Azure passato al cmdlet nel file JSON fornito.</span><span class="sxs-lookup"><span data-stu-id="d321a-111">This example saves the Azure context that is passed through to the cmdlet to the JSON file provided.</span></span>

## <span data-ttu-id="d321a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d321a-112">PARAMETERS</span></span>

### <span data-ttu-id="d321a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d321a-113">-DefaultProfile</span></span>
<span data-ttu-id="d321a-114">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d321a-114">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d321a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d321a-115">-Force</span></span>
<span data-ttu-id="d321a-116">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="d321a-116">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="d321a-117">-Path</span><span class="sxs-lookup"><span data-stu-id="d321a-117">-Path</span></span>
<span data-ttu-id="d321a-118">Specifica il percorso del file in cui salvare le informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d321a-118">Specifies the path of the file to which to save authentication information.</span></span>

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

### <span data-ttu-id="d321a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="d321a-119">-Profile</span></span>
<span data-ttu-id="d321a-120">Specifica il contesto Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d321a-120">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="d321a-121">Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d321a-121">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

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

### <span data-ttu-id="d321a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d321a-122">-Confirm</span></span>
<span data-ttu-id="d321a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d321a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d321a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d321a-124">-WhatIf</span></span>
<span data-ttu-id="d321a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d321a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d321a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d321a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d321a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d321a-127">CommonParameters</span></span>
<span data-ttu-id="d321a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d321a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d321a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d321a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d321a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d321a-130">INPUTS</span></span>

### <span data-ttu-id="d321a-131">Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="d321a-131">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>

## <span data-ttu-id="d321a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d321a-132">OUTPUTS</span></span>

### <span data-ttu-id="d321a-133">Microsoft. Azure. Commands. profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="d321a-133">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="d321a-134">Note</span><span class="sxs-lookup"><span data-stu-id="d321a-134">NOTES</span></span>

## <span data-ttu-id="d321a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d321a-135">RELATED LINKS</span></span>

