---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/clear-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Clear-AzureRmDefault.md
ms.openlocfilehash: 4f3a463f8ae03dcbefaf9588ca196f01955070ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508076"
---
# <span data-ttu-id="988dd-101">Clear-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="988dd-101">Clear-AzureRmDefault</span></span>

## <span data-ttu-id="988dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="988dd-102">SYNOPSIS</span></span>
<span data-ttu-id="988dd-103">Cancella le impostazioni predefinite impostate dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="988dd-103">Clears the defaults set by the user in the current context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="988dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="988dd-104">SYNTAX</span></span>

```
Clear-AzureRmDefault [-ResourceGroup] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="988dd-105">DESCRIPTION</span></span>
<span data-ttu-id="988dd-106">Il cmdlet Clear-AzureRmDefault rimuove i valori predefiniti impostati dall'utente in base ai parametri di switch specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="988dd-106">The Clear-AzureRmDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="988dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="988dd-107">EXAMPLES</span></span>

### <span data-ttu-id="988dd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="988dd-108">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault
```

<span data-ttu-id="988dd-109">Questo comando rimuove tutti i valori predefiniti impostati dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="988dd-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="988dd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="988dd-110">Example 1</span></span>
```
PS C:\> Clear-AzureRmDefault -ResourceGroup
```

<span data-ttu-id="988dd-111">Questo comando rimuove il gruppo di risorse predefinito impostato dall'utente nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="988dd-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="988dd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="988dd-112">PARAMETERS</span></span>

### <span data-ttu-id="988dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988dd-113">-DefaultProfile</span></span>
<span data-ttu-id="988dd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="988dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="988dd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="988dd-115">-Force</span></span>
<span data-ttu-id="988dd-116">Rimuovere tutte le impostazioni predefinite se non è specificato alcun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="988dd-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="988dd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="988dd-117">-PassThru</span></span>
<span data-ttu-id="988dd-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="988dd-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="988dd-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="988dd-119">-ResourceGroup</span></span>
<span data-ttu-id="988dd-120">Cancellare un gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="988dd-120">Clear Default Resource Group</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="988dd-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="988dd-121">-Confirm</span></span>
<span data-ttu-id="988dd-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988dd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988dd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988dd-123">-WhatIf</span></span>
<span data-ttu-id="988dd-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="988dd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988dd-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="988dd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988dd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988dd-126">CommonParameters</span></span>
<span data-ttu-id="988dd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988dd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988dd-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988dd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988dd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="988dd-129">INPUTS</span></span>

### <span data-ttu-id="988dd-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="988dd-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="988dd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="988dd-131">OUTPUTS</span></span>

### <span data-ttu-id="988dd-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="988dd-132">System.Object</span></span>

## <span data-ttu-id="988dd-133">Note</span><span class="sxs-lookup"><span data-stu-id="988dd-133">NOTES</span></span>

## <span data-ttu-id="988dd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="988dd-134">RELATED LINKS</span></span>

