---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023777"
---
# <span data-ttu-id="517ae-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="517ae-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="517ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="517ae-102">SYNOPSIS</span></span>
<span data-ttu-id="517ae-103">Imposta la posizione, l'abbonamento, lo slot e l'account di archiviazione predefiniti per il servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="517ae-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="517ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="517ae-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="517ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="517ae-105">DESCRIPTION</span></span>
<span data-ttu-id="517ae-106">Il cmdlet **set-AzureServiceProject** imposta il percorso di distribuzione, lo slot, l'account di archiviazione e l'abbonamento per il servizio corrente.</span><span class="sxs-lookup"><span data-stu-id="517ae-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="517ae-107">Questi valori vengono usati ogni volta che il servizio viene pubblicato nel cloud.</span><span class="sxs-lookup"><span data-stu-id="517ae-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="517ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="517ae-108">EXAMPLES</span></span>

### <span data-ttu-id="517ae-109">Esempio 1: impostazioni di base</span><span class="sxs-lookup"><span data-stu-id="517ae-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="517ae-110">Imposta il percorso di distribuzione per il servizio nell'area Nord America centrale.</span><span class="sxs-lookup"><span data-stu-id="517ae-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="517ae-111">Imposta lo slot di distribuzione su Production.</span><span class="sxs-lookup"><span data-stu-id="517ae-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="517ae-112">Imposta l'account di archiviazione che verrà usato per organizzare la definizione del servizio in myStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="517ae-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="517ae-113">Imposta la sottoscrizione che consentirà di ospitare il servizio in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="517ae-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="517ae-114">Ogni volta che il servizio viene pubblicato nel cloud, sarà ospitato in un centro dati nell'area nord-centrale degli Stati Uniti, che aggiornerà lo slot di distribuzione e userà l'account di sottoscrizione e archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="517ae-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="517ae-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="517ae-115">PARAMETERS</span></span>

### <span data-ttu-id="517ae-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="517ae-116">-Location</span></span>
<span data-ttu-id="517ae-117">Area geografica in cui verrà ospitato il servizio.</span><span class="sxs-lookup"><span data-stu-id="517ae-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="517ae-118">Questo valore viene usato ogni volta che il servizio viene pubblicato nel cloud.</span><span class="sxs-lookup"><span data-stu-id="517ae-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="517ae-119">I valori possibili sono: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span><span class="sxs-lookup"><span data-stu-id="517ae-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

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

### <span data-ttu-id="517ae-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="517ae-120">-PassThru</span></span>
<span data-ttu-id="517ae-121">Indica che questo cmdlet restituisce un oggetto che rappresenta l'elemento in cui opera.</span><span class="sxs-lookup"><span data-stu-id="517ae-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="517ae-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="517ae-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="517ae-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="517ae-123">-Profile</span></span>
<span data-ttu-id="517ae-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="517ae-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="517ae-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="517ae-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="517ae-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="517ae-126">-Slot</span></span>
<span data-ttu-id="517ae-127">Slot (produzione o staging) in cui verrà ospitato il servizio.</span><span class="sxs-lookup"><span data-stu-id="517ae-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="517ae-128">Questo valore viene usato ogni volta che il servizio viene pubblicato nel cloud.</span><span class="sxs-lookup"><span data-stu-id="517ae-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="517ae-129">I valori possibili sono: produzione, staging.</span><span class="sxs-lookup"><span data-stu-id="517ae-129">Possible values are: Production, Staging.</span></span>

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

### <span data-ttu-id="517ae-130">-Spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="517ae-130">-Storage</span></span>
<span data-ttu-id="517ae-131">Account di archiviazione da usare quando si carica il pacchetto del servizio nel cloud.</span><span class="sxs-lookup"><span data-stu-id="517ae-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="517ae-132">Se l'account di archiviazione non esiste, verrà creato quando il servizio viene pubblicato nel cloud.</span><span class="sxs-lookup"><span data-stu-id="517ae-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

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

### <span data-ttu-id="517ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517ae-133">CommonParameters</span></span>
<span data-ttu-id="517ae-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="517ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517ae-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517ae-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="517ae-136">INPUTS</span></span>

## <span data-ttu-id="517ae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="517ae-137">OUTPUTS</span></span>

## <span data-ttu-id="517ae-138">Note</span><span class="sxs-lookup"><span data-stu-id="517ae-138">NOTES</span></span>
* <span data-ttu-id="517ae-139">node-dev, php-dev, python-dev</span><span class="sxs-lookup"><span data-stu-id="517ae-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="517ae-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="517ae-140">RELATED LINKS</span></span>

[<span data-ttu-id="517ae-141">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="517ae-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="517ae-142">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="517ae-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="517ae-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="517ae-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


