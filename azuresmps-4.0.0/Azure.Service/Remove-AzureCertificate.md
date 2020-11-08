---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029629"
---
# <span data-ttu-id="9fa5b-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa5b-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="9fa5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fa5b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa5b-103">Rimuove un certificato da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="9fa5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fa5b-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa5b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fa5b-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa5b-106">Il cmdlet **Remove-AzureCertificate** rimuove un certificato da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="9fa5b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fa5b-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa5b-108">Esempio 1: rimuovere un certificato da un servizio</span><span class="sxs-lookup"><span data-stu-id="9fa5b-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="9fa5b-109">Questo comando rimuove l'oggetto certificato con l'identificazione personale specificata dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="9fa5b-110">Esempio 2: rimuovere tutti i certificati da un servizio</span><span class="sxs-lookup"><span data-stu-id="9fa5b-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="9fa5b-111">Questo comando recupera tutti i certificati dal servizio denominato ContosoService usando il cmdlet **Get-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="9fa5b-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="9fa5b-112">Il comando passa ogni certificato al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9fa5b-113">Questo cmdlet rimuove ogni certificato dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="9fa5b-114">Esempio 3: rimuovere tutti i certificati da un servizio che usa un algoritmo di identificazione personale specifico</span><span class="sxs-lookup"><span data-stu-id="9fa5b-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="9fa5b-115">Questo comando ottiene tutti i certificati del servizio denominato ContosoService che usano l'algoritmo di identificazione personale SHA1.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="9fa5b-116">Il comando passa ogni certificato al cmdlet corrente, che rimuove ogni certificato.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="9fa5b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fa5b-117">PARAMETERS</span></span>

### <span data-ttu-id="9fa5b-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9fa5b-118">-InformationAction</span></span>
<span data-ttu-id="9fa5b-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9fa5b-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9fa5b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9fa5b-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="9fa5b-121">Continue</span></span>
- <span data-ttu-id="9fa5b-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="9fa5b-122">Ignore</span></span>
- <span data-ttu-id="9fa5b-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="9fa5b-123">Inquire</span></span>
- <span data-ttu-id="9fa5b-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9fa5b-124">SilentlyContinue</span></span>
- <span data-ttu-id="9fa5b-125">Stop</span><span class="sxs-lookup"><span data-stu-id="9fa5b-125">Stop</span></span>
- <span data-ttu-id="9fa5b-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="9fa5b-126">Suspend</span></span>

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

### <span data-ttu-id="9fa5b-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9fa5b-127">-InformationVariable</span></span>
<span data-ttu-id="9fa5b-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9fa5b-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="9fa5b-129">-Profile</span></span>
<span data-ttu-id="9fa5b-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9fa5b-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9fa5b-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9fa5b-132">-ServiceName</span></span>
<span data-ttu-id="9fa5b-133">Specifica il nome del servizio Azure da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="9fa5b-134">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="9fa5b-134">-Thumbprint</span></span>
<span data-ttu-id="9fa5b-135">Specifica l'identificazione personale del certificato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa5b-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9fa5b-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="9fa5b-137">Specifica l'algoritmo usato per creare l'identificazione personale del certificato.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa5b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa5b-138">CommonParameters</span></span>
<span data-ttu-id="9fa5b-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa5b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa5b-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa5b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa5b-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fa5b-141">INPUTS</span></span>

## <span data-ttu-id="9fa5b-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fa5b-142">OUTPUTS</span></span>

### <span data-ttu-id="9fa5b-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="9fa5b-143">ManagementOperationContext</span></span>

## <span data-ttu-id="9fa5b-144">Note</span><span class="sxs-lookup"><span data-stu-id="9fa5b-144">NOTES</span></span>

## <span data-ttu-id="9fa5b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fa5b-145">RELATED LINKS</span></span>

[<span data-ttu-id="9fa5b-146">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa5b-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="9fa5b-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="9fa5b-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="9fa5b-148">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="9fa5b-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


