---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023629"
---
# <span data-ttu-id="32a20-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="32a20-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="32a20-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32a20-102">SYNOPSIS</span></span>
<span data-ttu-id="32a20-103">Ottiene un oggetto Group Affinity di Azure.</span><span class="sxs-lookup"><span data-stu-id="32a20-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="32a20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32a20-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="32a20-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32a20-105">DESCRIPTION</span></span>
<span data-ttu-id="32a20-106">Il cmdlet **Get-AzureAffinityGroup** ottiene un gruppo di affinità Azure.</span><span class="sxs-lookup"><span data-stu-id="32a20-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="32a20-107">L'oggetto gruppo affinità include il nome del gruppo di affinità, la posizione, l'etichetta, la descrizione e i servizi di archiviazione e ospitati che fanno parte del gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="32a20-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="32a20-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32a20-108">EXAMPLES</span></span>

### <span data-ttu-id="32a20-109">Esempio 1: ottenere le proprietà di un gruppo di affinità</span><span class="sxs-lookup"><span data-stu-id="32a20-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="32a20-110">Questo comando consente di ottenere le proprietà del gruppo affinità denominato South01.</span><span class="sxs-lookup"><span data-stu-id="32a20-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="32a20-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32a20-111">PARAMETERS</span></span>

### <span data-ttu-id="32a20-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="32a20-112">-InformationAction</span></span>
<span data-ttu-id="32a20-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="32a20-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="32a20-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="32a20-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32a20-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="32a20-115">Continue</span></span>
- <span data-ttu-id="32a20-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="32a20-116">Ignore</span></span>
- <span data-ttu-id="32a20-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="32a20-117">Inquire</span></span>
- <span data-ttu-id="32a20-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="32a20-118">SilentlyContinue</span></span>
- <span data-ttu-id="32a20-119">Stop</span><span class="sxs-lookup"><span data-stu-id="32a20-119">Stop</span></span>
- <span data-ttu-id="32a20-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="32a20-120">Suspend</span></span>

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

### <span data-ttu-id="32a20-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="32a20-121">-InformationVariable</span></span>
<span data-ttu-id="32a20-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="32a20-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="32a20-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="32a20-123">-Name</span></span>
<span data-ttu-id="32a20-124">Specifica il nome del gruppo di affinità ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32a20-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="32a20-125">I nomi dei gruppi di affinità creati tramite il portale di gestione sono in genere GUID.</span><span class="sxs-lookup"><span data-stu-id="32a20-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="32a20-126">La porta di gestione Mostra l'etichetta del gruppo affinità.</span><span class="sxs-lookup"><span data-stu-id="32a20-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a20-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="32a20-127">-Profile</span></span>
<span data-ttu-id="32a20-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32a20-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32a20-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="32a20-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32a20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a20-130">CommonParameters</span></span>
<span data-ttu-id="32a20-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32a20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a20-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a20-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a20-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32a20-133">INPUTS</span></span>

## <span data-ttu-id="32a20-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32a20-134">OUTPUTS</span></span>

### <span data-ttu-id="32a20-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="32a20-135">AffinityGroup</span></span>

## <span data-ttu-id="32a20-136">Note</span><span class="sxs-lookup"><span data-stu-id="32a20-136">NOTES</span></span>

## <span data-ttu-id="32a20-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32a20-137">RELATED LINKS</span></span>

[<span data-ttu-id="32a20-138">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="32a20-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="32a20-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="32a20-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="32a20-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="32a20-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


