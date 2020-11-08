---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023608"
---
# <span data-ttu-id="1c321-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="1c321-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="1c321-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c321-102">SYNOPSIS</span></span>
<span data-ttu-id="1c321-103">Ottiene informazioni sugli eventi avviati da Azure che influiscono sulle macchine virtuali e sui servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="1c321-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="1c321-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c321-104">SYNTAX</span></span>

### <span data-ttu-id="1c321-105">GetDeploymentEventBySlot (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c321-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1c321-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="1c321-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c321-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c321-107">DESCRIPTION</span></span>
<span data-ttu-id="1c321-108">Il cmdlet **Get-AzureDeploymentEvent** ottiene le informazioni relative agli eventi avviati da Azure che impattano le macchine virtuali e i servizi cloud.</span><span class="sxs-lookup"><span data-stu-id="1c321-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="1c321-109">Questi eventi includono eventi di manutenzione pianificata.</span><span class="sxs-lookup"><span data-stu-id="1c321-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="1c321-110">Questo cmdlet restituisce un elenco di eventi che identificano l'istanza del ruolo o la macchina virtuale interessata, il motivo dell'impatto e l'ora di inizio dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1c321-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="1c321-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c321-111">EXAMPLES</span></span>

### <span data-ttu-id="1c321-112">1:</span><span class="sxs-lookup"><span data-stu-id="1c321-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="1c321-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c321-113">PARAMETERS</span></span>

### <span data-ttu-id="1c321-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1c321-114">-DeploymentName</span></span>
<span data-ttu-id="1c321-115">Specifica il nome della distribuzione per cui questo cmdlet ottiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1c321-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c321-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1c321-116">-EndTime</span></span>
<span data-ttu-id="1c321-117">Specifica il tempo di fine per gli eventi pianificati ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c321-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c321-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1c321-118">-InformationAction</span></span>
<span data-ttu-id="1c321-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="1c321-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1c321-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1c321-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c321-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="1c321-121">Continue</span></span>
- <span data-ttu-id="1c321-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="1c321-122">Ignore</span></span>
- <span data-ttu-id="1c321-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="1c321-123">Inquire</span></span>
- <span data-ttu-id="1c321-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1c321-124">SilentlyContinue</span></span>
- <span data-ttu-id="1c321-125">Stop</span><span class="sxs-lookup"><span data-stu-id="1c321-125">Stop</span></span>
- <span data-ttu-id="1c321-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="1c321-126">Suspend</span></span>

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

### <span data-ttu-id="1c321-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1c321-127">-InformationVariable</span></span>
<span data-ttu-id="1c321-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="1c321-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1c321-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="1c321-129">-Profile</span></span>
<span data-ttu-id="1c321-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c321-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c321-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1c321-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c321-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1c321-132">-ServiceName</span></span>
<span data-ttu-id="1c321-133">Specifica il nome del servizio ospitato per il quale questo cmdlet ottiene gli eventi pianificati.</span><span class="sxs-lookup"><span data-stu-id="1c321-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

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

### <span data-ttu-id="1c321-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="1c321-134">-Slot</span></span>
<span data-ttu-id="1c321-135">Specifica l'ambiente della distribuzione per cui questo cmdlet ottiene gli eventi pianificati.</span><span class="sxs-lookup"><span data-stu-id="1c321-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="1c321-136">I valori validi sono: staging e produzione.</span><span class="sxs-lookup"><span data-stu-id="1c321-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="1c321-137">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="1c321-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c321-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1c321-138">-StartTime</span></span>
<span data-ttu-id="1c321-139">Specifica l'ora di inizio per gli eventi pianificati ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c321-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c321-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c321-140">CommonParameters</span></span>
<span data-ttu-id="1c321-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c321-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c321-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c321-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c321-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c321-143">INPUTS</span></span>

## <span data-ttu-id="1c321-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c321-144">OUTPUTS</span></span>

## <span data-ttu-id="1c321-145">Note</span><span class="sxs-lookup"><span data-stu-id="1c321-145">NOTES</span></span>

## <span data-ttu-id="1c321-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c321-146">RELATED LINKS</span></span>

[<span data-ttu-id="1c321-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1c321-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


