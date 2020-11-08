---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023604"
---
# <span data-ttu-id="e1f75-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e1f75-101">Get-AzureDns</span></span>

## <span data-ttu-id="e1f75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1f75-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f75-103">Ottiene le impostazioni DNS per una distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f75-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="e1f75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1f75-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e1f75-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1f75-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f75-106">Il cmdlet **Get-AzureDns** ottiene le impostazioni DNS per una distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f75-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="e1f75-107">Il cmdlet restituisce il nome descrittivo e l'indirizzo IP del server DNS in un oggetto impostazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="e1f75-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="e1f75-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1f75-108">EXAMPLES</span></span>

### <span data-ttu-id="e1f75-109">Esempio 1: ottenere le impostazioni DNS</span><span class="sxs-lookup"><span data-stu-id="e1f75-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="e1f75-110">Questo comando usa il cmdlet **Get-AzureDeployment** per ottenere la distribuzione di produzione del servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="e1f75-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="e1f75-111">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1f75-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e1f75-112">Il cmdlet corrente ottiene le impostazioni DNS.</span><span class="sxs-lookup"><span data-stu-id="e1f75-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="e1f75-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1f75-113">PARAMETERS</span></span>

### <span data-ttu-id="e1f75-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="e1f75-114">-DnsSettings</span></span>
<span data-ttu-id="e1f75-115">Specifica un oggetto **DnsSettings** .</span><span class="sxs-lookup"><span data-stu-id="e1f75-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f75-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e1f75-116">-InformationAction</span></span>
<span data-ttu-id="e1f75-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e1f75-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e1f75-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1f75-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e1f75-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="e1f75-119">Continue</span></span>
- <span data-ttu-id="e1f75-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="e1f75-120">Ignore</span></span>
- <span data-ttu-id="e1f75-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e1f75-121">Inquire</span></span>
- <span data-ttu-id="e1f75-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e1f75-122">SilentlyContinue</span></span>
- <span data-ttu-id="e1f75-123">Stop</span><span class="sxs-lookup"><span data-stu-id="e1f75-123">Stop</span></span>
- <span data-ttu-id="e1f75-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e1f75-124">Suspend</span></span>

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

### <span data-ttu-id="e1f75-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e1f75-125">-InformationVariable</span></span>
<span data-ttu-id="e1f75-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e1f75-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e1f75-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f75-127">CommonParameters</span></span>
<span data-ttu-id="e1f75-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f75-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f75-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f75-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f75-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1f75-130">INPUTS</span></span>

## <span data-ttu-id="e1f75-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1f75-131">OUTPUTS</span></span>

## <span data-ttu-id="e1f75-132">Note</span><span class="sxs-lookup"><span data-stu-id="e1f75-132">NOTES</span></span>

## <span data-ttu-id="e1f75-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1f75-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1f75-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e1f75-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="e1f75-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e1f75-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="e1f75-136">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e1f75-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="e1f75-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e1f75-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="e1f75-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e1f75-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


