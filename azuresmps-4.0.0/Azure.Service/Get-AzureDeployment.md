---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029817"
---
# <span data-ttu-id="ff181-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff181-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="ff181-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff181-102">SYNOPSIS</span></span>
<span data-ttu-id="ff181-103">Ottiene i dettagli di una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ff181-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="ff181-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff181-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff181-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff181-105">DESCRIPTION</span></span>
<span data-ttu-id="ff181-106">Il cmdlet **Get-AzureDeployment** ottiene i dettagli di una distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff181-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="ff181-107">Specificare il nome del servizio Azure e lo slot della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ff181-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="ff181-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff181-108">EXAMPLES</span></span>

### <span data-ttu-id="ff181-109">Esempio 1: ottenere informazioni dettagliate per una distribuzione di produzione</span><span class="sxs-lookup"><span data-stu-id="ff181-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="ff181-110">Questo comando restituisce i dettagli della distribuzione per il servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="ff181-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="ff181-111">Questo comando non specifica uno slot.</span><span class="sxs-lookup"><span data-stu-id="ff181-111">This command does not specify a slot.</span></span>
<span data-ttu-id="ff181-112">Il comando usa quindi il valore predefinito di Production.</span><span class="sxs-lookup"><span data-stu-id="ff181-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="ff181-113">Esempio 2: ottenere informazioni dettagliate per una distribuzione di staging</span><span class="sxs-lookup"><span data-stu-id="ff181-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="ff181-114">Questo comando restituisce i dettagli della distribuzione della gestione temporanea di ContosoService.</span><span class="sxs-lookup"><span data-stu-id="ff181-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="ff181-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff181-115">PARAMETERS</span></span>

### <span data-ttu-id="ff181-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff181-116">-InformationAction</span></span>
<span data-ttu-id="ff181-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ff181-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff181-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff181-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff181-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="ff181-119">Continue</span></span>
- <span data-ttu-id="ff181-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="ff181-120">Ignore</span></span>
- <span data-ttu-id="ff181-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ff181-121">Inquire</span></span>
- <span data-ttu-id="ff181-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff181-122">SilentlyContinue</span></span>
- <span data-ttu-id="ff181-123">Stop</span><span class="sxs-lookup"><span data-stu-id="ff181-123">Stop</span></span>
- <span data-ttu-id="ff181-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ff181-124">Suspend</span></span>

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

### <span data-ttu-id="ff181-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff181-125">-InformationVariable</span></span>
<span data-ttu-id="ff181-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ff181-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff181-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="ff181-127">-Profile</span></span>
<span data-ttu-id="ff181-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff181-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff181-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ff181-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff181-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ff181-130">-ServiceName</span></span>
<span data-ttu-id="ff181-131">Specifica il nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="ff181-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="ff181-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="ff181-132">-Slot</span></span>
<span data-ttu-id="ff181-133">Specifica l'ambiente della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ff181-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="ff181-134">I valori validi sono: staging o Production.</span><span class="sxs-lookup"><span data-stu-id="ff181-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="ff181-135">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="ff181-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff181-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff181-136">CommonParameters</span></span>
<span data-ttu-id="ff181-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff181-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff181-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff181-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff181-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff181-139">INPUTS</span></span>

## <span data-ttu-id="ff181-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff181-140">OUTPUTS</span></span>

## <span data-ttu-id="ff181-141">Note</span><span class="sxs-lookup"><span data-stu-id="ff181-141">NOTES</span></span>

## <span data-ttu-id="ff181-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff181-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff181-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="ff181-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="ff181-144">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff181-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="ff181-145">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff181-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="ff181-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff181-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="ff181-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="ff181-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


