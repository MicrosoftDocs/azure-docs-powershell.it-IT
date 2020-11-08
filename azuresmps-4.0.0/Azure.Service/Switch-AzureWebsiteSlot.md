---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023897"
---
# <span data-ttu-id="270de-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="270de-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="270de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="270de-102">SYNOPSIS</span></span>
<span data-ttu-id="270de-103">Scambia lo slot di produzione per un sito Web con un altro slot.</span><span class="sxs-lookup"><span data-stu-id="270de-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="270de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="270de-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="270de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="270de-105">DESCRIPTION</span></span>
<span data-ttu-id="270de-106">Il cmdlet **Switch-AzureWebsiteSlot** scambia lo slot di produzione per un sito Web con un altro slot.</span><span class="sxs-lookup"><span data-stu-id="270de-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="270de-107">Questo funziona con i siti Web con due solo slot.</span><span class="sxs-lookup"><span data-stu-id="270de-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="270de-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="270de-108">EXAMPLES</span></span>

### <span data-ttu-id="270de-109">Esempio 1: cambiare lo slot del sito Web</span><span class="sxs-lookup"><span data-stu-id="270de-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="270de-110">Cambiare lo slot di backup del sito Web di Azure con lo slot di produzione.</span><span class="sxs-lookup"><span data-stu-id="270de-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="270de-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="270de-111">PARAMETERS</span></span>

### <span data-ttu-id="270de-112">-Force</span><span class="sxs-lookup"><span data-stu-id="270de-112">-Force</span></span>
<span data-ttu-id="270de-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="270de-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="270de-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="270de-114">-Name</span></span>
<span data-ttu-id="270de-115">Nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="270de-115">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270de-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="270de-116">-Profile</span></span>
<span data-ttu-id="270de-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270de-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="270de-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="270de-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="270de-119">-SLOT1</span><span class="sxs-lookup"><span data-stu-id="270de-119">-Slot1</span></span>
<span data-ttu-id="270de-120">Specifica il primo slot.</span><span class="sxs-lookup"><span data-stu-id="270de-120">Specifies the first slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270de-121">-SLOT2</span><span class="sxs-lookup"><span data-stu-id="270de-121">-Slot2</span></span>
<span data-ttu-id="270de-122">Specifica il secondo slot.</span><span class="sxs-lookup"><span data-stu-id="270de-122">Specifies the second slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270de-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="270de-123">-Confirm</span></span>
<span data-ttu-id="270de-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270de-125">-WhatIf</span></span>
<span data-ttu-id="270de-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="270de-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="270de-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="270de-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270de-128">CommonParameters</span></span>
<span data-ttu-id="270de-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270de-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270de-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270de-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="270de-131">INPUTS</span></span>

## <span data-ttu-id="270de-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="270de-132">OUTPUTS</span></span>

## <span data-ttu-id="270de-133">Note</span><span class="sxs-lookup"><span data-stu-id="270de-133">NOTES</span></span>

## <span data-ttu-id="270de-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="270de-134">RELATED LINKS</span></span>

[<span data-ttu-id="270de-135">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="270de-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="270de-136">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="270de-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="270de-137">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="270de-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="270de-138">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="270de-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


