---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029607"
---
# <span data-ttu-id="3485e-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3485e-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="3485e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3485e-102">SYNOPSIS</span></span>
<span data-ttu-id="3485e-103">Rimuove un indirizzo IP riservato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="3485e-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="3485e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3485e-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3485e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3485e-105">DESCRIPTION</span></span>
<span data-ttu-id="3485e-106">Il cmdlet **Remove-AzureReservedIP** rimuove un indirizzo IP riservato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="3485e-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="3485e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3485e-107">EXAMPLES</span></span>

### <span data-ttu-id="3485e-108">Esempio 1: rimuovere un indirizzo IP riservato in base al nome</span><span class="sxs-lookup"><span data-stu-id="3485e-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="3485e-109">Questo comando rimuove un indirizzo IP riservato in base al nome.</span><span class="sxs-lookup"><span data-stu-id="3485e-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="3485e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3485e-110">PARAMETERS</span></span>

### <span data-ttu-id="3485e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3485e-111">-Force</span></span>
<span data-ttu-id="3485e-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3485e-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3485e-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3485e-113">-InformationAction</span></span>
<span data-ttu-id="3485e-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="3485e-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3485e-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3485e-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3485e-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="3485e-116">Continue</span></span>
- <span data-ttu-id="3485e-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="3485e-117">Ignore</span></span>
- <span data-ttu-id="3485e-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="3485e-118">Inquire</span></span>
- <span data-ttu-id="3485e-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3485e-119">SilentlyContinue</span></span>
- <span data-ttu-id="3485e-120">Stop</span><span class="sxs-lookup"><span data-stu-id="3485e-120">Stop</span></span>
- <span data-ttu-id="3485e-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="3485e-121">Suspend</span></span>

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

### <span data-ttu-id="3485e-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3485e-122">-InformationVariable</span></span>
<span data-ttu-id="3485e-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3485e-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3485e-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="3485e-124">-Profile</span></span>
<span data-ttu-id="3485e-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3485e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3485e-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3485e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3485e-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="3485e-127">-ReservedIPName</span></span>
<span data-ttu-id="3485e-128">Specifica il nome dell'indirizzo IP riservato.</span><span class="sxs-lookup"><span data-stu-id="3485e-128">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="3485e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3485e-129">CommonParameters</span></span>
<span data-ttu-id="3485e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3485e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3485e-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3485e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3485e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3485e-132">INPUTS</span></span>

## <span data-ttu-id="3485e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3485e-133">OUTPUTS</span></span>

## <span data-ttu-id="3485e-134">Note</span><span class="sxs-lookup"><span data-stu-id="3485e-134">NOTES</span></span>

## <span data-ttu-id="3485e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3485e-135">RELATED LINKS</span></span>

[<span data-ttu-id="3485e-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3485e-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="3485e-137">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3485e-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="3485e-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="3485e-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


