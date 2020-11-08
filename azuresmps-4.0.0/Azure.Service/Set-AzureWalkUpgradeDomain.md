---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023744"
---
# <span data-ttu-id="b5be5-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="b5be5-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="b5be5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5be5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5be5-103">Consente di aggirare il dominio di aggiornamento specificato.</span><span class="sxs-lookup"><span data-stu-id="b5be5-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="b5be5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5be5-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5be5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5be5-105">DESCRIPTION</span></span>
<span data-ttu-id="b5be5-106">Il cmdlet **set-AzureWalkUpgradeDomain** avvia l'aggiornamento effettivo di una distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5be5-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="b5be5-107">Il pacchetto e la configurazione di aggiornamento vengono impostati usando il cmdlet **set-AzureDeployment** con l'opzione-upgrade.</span><span class="sxs-lookup"><span data-stu-id="b5be5-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="b5be5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5be5-108">EXAMPLES</span></span>

### <span data-ttu-id="b5be5-109">Esempio 1: avviare un aggiornamento di una distribuzione di produzione</span><span class="sxs-lookup"><span data-stu-id="b5be5-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="b5be5-110">Questo comando avvia l'aggiornamento del dominio di aggiornamento 2 della distribuzione della produzione del servizio MySvc1.</span><span class="sxs-lookup"><span data-stu-id="b5be5-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="b5be5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5be5-111">PARAMETERS</span></span>

### <span data-ttu-id="b5be5-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="b5be5-112">-DomainNumber</span></span>
<span data-ttu-id="b5be5-113">Specifica il dominio di aggiornamento da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b5be5-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5be5-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5be5-114">-InformationAction</span></span>
<span data-ttu-id="b5be5-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b5be5-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5be5-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5be5-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5be5-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="b5be5-117">Continue</span></span>
- <span data-ttu-id="b5be5-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="b5be5-118">Ignore</span></span>
- <span data-ttu-id="b5be5-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b5be5-119">Inquire</span></span>
- <span data-ttu-id="b5be5-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5be5-120">SilentlyContinue</span></span>
- <span data-ttu-id="b5be5-121">Stop</span><span class="sxs-lookup"><span data-stu-id="b5be5-121">Stop</span></span>
- <span data-ttu-id="b5be5-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b5be5-122">Suspend</span></span>

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

### <span data-ttu-id="b5be5-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5be5-123">-InformationVariable</span></span>
<span data-ttu-id="b5be5-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b5be5-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5be5-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="b5be5-125">-Profile</span></span>
<span data-ttu-id="b5be5-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5be5-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5be5-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b5be5-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5be5-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b5be5-128">-ServiceName</span></span>
<span data-ttu-id="b5be5-129">Specifica il nome del servizio Microsoft Azure da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b5be5-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

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

### <span data-ttu-id="b5be5-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="b5be5-130">-Slot</span></span>
<span data-ttu-id="b5be5-131">Specifica l'ambiente della distribuzione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="b5be5-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="b5be5-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5be5-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5be5-133">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="b5be5-133">Staging</span></span>
- <span data-ttu-id="b5be5-134">Produzione</span><span class="sxs-lookup"><span data-stu-id="b5be5-134">Production</span></span>

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

### <span data-ttu-id="b5be5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5be5-135">CommonParameters</span></span>
<span data-ttu-id="b5be5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5be5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5be5-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5be5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5be5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5be5-138">INPUTS</span></span>

## <span data-ttu-id="b5be5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5be5-139">OUTPUTS</span></span>

### <span data-ttu-id="b5be5-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b5be5-140">ManagementOperationContext</span></span>

## <span data-ttu-id="b5be5-141">Note</span><span class="sxs-lookup"><span data-stu-id="b5be5-141">NOTES</span></span>

## <span data-ttu-id="b5be5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5be5-142">RELATED LINKS</span></span>

[<span data-ttu-id="b5be5-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b5be5-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


