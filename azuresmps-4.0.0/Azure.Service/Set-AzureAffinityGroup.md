---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029893"
---
# <span data-ttu-id="52b2f-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="52b2f-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="52b2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="52b2f-103">Modifica le proprietà di un gruppo di affinità.</span><span class="sxs-lookup"><span data-stu-id="52b2f-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="52b2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52b2f-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="52b2f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="52b2f-106">Il cmdlet **set-AzureAffinityGroup** modifica le proprietà di un gruppo di affinità di Azure.</span><span class="sxs-lookup"><span data-stu-id="52b2f-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="52b2f-107">È possibile modificare l'etichetta e la descrizione.</span><span class="sxs-lookup"><span data-stu-id="52b2f-107">You can change the label and the description.</span></span>

## <span data-ttu-id="52b2f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52b2f-108">EXAMPLES</span></span>

### <span data-ttu-id="52b2f-109">Esempio 1: modificare un gruppo di affinità</span><span class="sxs-lookup"><span data-stu-id="52b2f-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="52b2f-110">Questo comando modifica l'etichetta del gruppo di affinità denominato South01 in SouthUSProduction il comando modifica anche la descrizione.</span><span class="sxs-lookup"><span data-stu-id="52b2f-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="52b2f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52b2f-111">PARAMETERS</span></span>

### <span data-ttu-id="52b2f-112">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="52b2f-112">-Description</span></span>
<span data-ttu-id="52b2f-113">Specifica la descrizione del gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="52b2f-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="52b2f-114">La descrizione può contenere fino a 1024 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="52b2f-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b2f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="52b2f-115">-InformationAction</span></span>
<span data-ttu-id="52b2f-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="52b2f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="52b2f-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="52b2f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="52b2f-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="52b2f-118">Continue</span></span>
- <span data-ttu-id="52b2f-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="52b2f-119">Ignore</span></span>
- <span data-ttu-id="52b2f-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="52b2f-120">Inquire</span></span>
- <span data-ttu-id="52b2f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="52b2f-121">SilentlyContinue</span></span>
- <span data-ttu-id="52b2f-122">Stop</span><span class="sxs-lookup"><span data-stu-id="52b2f-122">Stop</span></span>
- <span data-ttu-id="52b2f-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="52b2f-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b2f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="52b2f-124">-InformationVariable</span></span>
<span data-ttu-id="52b2f-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="52b2f-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b2f-126">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="52b2f-126">-Label</span></span>
<span data-ttu-id="52b2f-127">Specifica un'etichetta per il gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="52b2f-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="52b2f-128">L'etichetta può contenere fino a 100 caratteri di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="52b2f-128">The label can be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b2f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="52b2f-129">-Name</span></span>
<span data-ttu-id="52b2f-130">Specifica il nome del gruppo di affinità modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b2f-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52b2f-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="52b2f-131">-Profile</span></span>
<span data-ttu-id="52b2f-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b2f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52b2f-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="52b2f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52b2f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b2f-134">CommonParameters</span></span>
<span data-ttu-id="52b2f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b2f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b2f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b2f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b2f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52b2f-137">INPUTS</span></span>

## <span data-ttu-id="52b2f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52b2f-138">OUTPUTS</span></span>

## <span data-ttu-id="52b2f-139">Note</span><span class="sxs-lookup"><span data-stu-id="52b2f-139">NOTES</span></span>

## <span data-ttu-id="52b2f-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52b2f-140">RELATED LINKS</span></span>

[<span data-ttu-id="52b2f-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="52b2f-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="52b2f-142">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="52b2f-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="52b2f-143">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="52b2f-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


