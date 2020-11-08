---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029818"
---
# <span data-ttu-id="07eda-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="07eda-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="07eda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07eda-102">SYNOPSIS</span></span>
<span data-ttu-id="07eda-103">Ottiene un oggetto certificate da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="07eda-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="07eda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07eda-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="07eda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07eda-105">DESCRIPTION</span></span>
<span data-ttu-id="07eda-106">Il cmdlet **Get-AzureCertificate** ottiene un oggetto certificate da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="07eda-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="07eda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07eda-107">EXAMPLES</span></span>

### <span data-ttu-id="07eda-108">Esempio 1: ottenere i certificati da un servizio</span><span class="sxs-lookup"><span data-stu-id="07eda-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="07eda-109">Questo comando ottiene gli oggetti certificato dal servizio denominato ContosoService e li archivia nella variabile $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="07eda-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="07eda-110">Esempio 2: ottenere un certificato da un servizio</span><span class="sxs-lookup"><span data-stu-id="07eda-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="07eda-111">Questo comando ottiene l'oggetto certificato identificato dall'identificazione personale specificata dal servizio denominato ContosoService e lo archivia nella variabile $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="07eda-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="07eda-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07eda-112">PARAMETERS</span></span>

### <span data-ttu-id="07eda-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="07eda-113">-InformationAction</span></span>
<span data-ttu-id="07eda-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="07eda-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="07eda-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="07eda-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="07eda-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="07eda-116">Continue</span></span>
- <span data-ttu-id="07eda-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="07eda-117">Ignore</span></span>
- <span data-ttu-id="07eda-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="07eda-118">Inquire</span></span>
- <span data-ttu-id="07eda-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="07eda-119">SilentlyContinue</span></span>
- <span data-ttu-id="07eda-120">Stop</span><span class="sxs-lookup"><span data-stu-id="07eda-120">Stop</span></span>
- <span data-ttu-id="07eda-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="07eda-121">Suspend</span></span>

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

### <span data-ttu-id="07eda-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="07eda-122">-InformationVariable</span></span>
<span data-ttu-id="07eda-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="07eda-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="07eda-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="07eda-124">-Profile</span></span>
<span data-ttu-id="07eda-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07eda-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07eda-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="07eda-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07eda-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="07eda-127">-ServiceName</span></span>
<span data-ttu-id="07eda-128">Specifica il nome del servizio Azure da cui questo cmdlet ottiene un certificato.</span><span class="sxs-lookup"><span data-stu-id="07eda-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

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

### <span data-ttu-id="07eda-129">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="07eda-129">-Thumbprint</span></span>
<span data-ttu-id="07eda-130">Specifica l'identificazione personale del certificato ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07eda-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07eda-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="07eda-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="07eda-132">Specifica l'algoritmo usato per creare l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="07eda-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

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

### <span data-ttu-id="07eda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07eda-133">CommonParameters</span></span>
<span data-ttu-id="07eda-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07eda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07eda-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07eda-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07eda-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07eda-136">INPUTS</span></span>

## <span data-ttu-id="07eda-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07eda-137">OUTPUTS</span></span>

### <span data-ttu-id="07eda-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="07eda-138">CertificateContext</span></span>

## <span data-ttu-id="07eda-139">Note</span><span class="sxs-lookup"><span data-stu-id="07eda-139">NOTES</span></span>

## <span data-ttu-id="07eda-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07eda-140">RELATED LINKS</span></span>

[<span data-ttu-id="07eda-141">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="07eda-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="07eda-142">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="07eda-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="07eda-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="07eda-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


