---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023745"
---
# <span data-ttu-id="71a05-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="71a05-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="71a05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71a05-102">SYNOPSIS</span></span>
<span data-ttu-id="71a05-103">Aggiorna le impostazioni di rete virtuale per un servizio cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="71a05-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="71a05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71a05-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="71a05-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71a05-105">DESCRIPTION</span></span>
<span data-ttu-id="71a05-106">Il cmdlet **set-AzureVNetConfig** aggiorna la configurazione di rete per l'abbonamento Azure corrente specificando un percorso di un file di configurazione di rete (. netcfg).</span><span class="sxs-lookup"><span data-stu-id="71a05-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="71a05-107">Il file di configurazione della rete definisce i server DNS e le subnet per i servizi cloud all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="71a05-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="71a05-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71a05-108">EXAMPLES</span></span>

### <span data-ttu-id="71a05-109">Esempio 1: aggiornare la configurazione di rete dell'abbonamento Azure a un file locale</span><span class="sxs-lookup"><span data-stu-id="71a05-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="71a05-110">Questo comando Aggiorna la configurazione di rete dell'abbonamento a Microsoft Azure corrente nel file locale "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="71a05-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="71a05-111">Esempio 2: impostare l'abbonamento a Azure e quindi aggiornare la configurazione di rete</span><span class="sxs-lookup"><span data-stu-id="71a05-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="71a05-112">Questo esempio imposta l'abbonamento a Microsoft Azure e quindi aggiorna la configurazione di rete di tale abbonamento usando la configurazione definita nel file locale "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="71a05-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="71a05-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71a05-113">PARAMETERS</span></span>

### <span data-ttu-id="71a05-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="71a05-114">-ConfigurationPath</span></span>
<span data-ttu-id="71a05-115">Specifica il percorso e il nome file di un file di configurazione di rete (. netcfg).</span><span class="sxs-lookup"><span data-stu-id="71a05-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a05-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="71a05-116">-InformationAction</span></span>
<span data-ttu-id="71a05-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="71a05-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="71a05-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="71a05-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71a05-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="71a05-119">Continue</span></span>
- <span data-ttu-id="71a05-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="71a05-120">Ignore</span></span>
- <span data-ttu-id="71a05-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="71a05-121">Inquire</span></span>
- <span data-ttu-id="71a05-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="71a05-122">SilentlyContinue</span></span>
- <span data-ttu-id="71a05-123">Stop</span><span class="sxs-lookup"><span data-stu-id="71a05-123">Stop</span></span>
- <span data-ttu-id="71a05-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="71a05-124">Suspend</span></span>

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

### <span data-ttu-id="71a05-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="71a05-125">-InformationVariable</span></span>
<span data-ttu-id="71a05-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="71a05-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="71a05-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="71a05-127">-Profile</span></span>
<span data-ttu-id="71a05-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71a05-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71a05-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="71a05-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71a05-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a05-130">CommonParameters</span></span>
<span data-ttu-id="71a05-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a05-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a05-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a05-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a05-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71a05-133">INPUTS</span></span>

## <span data-ttu-id="71a05-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71a05-134">OUTPUTS</span></span>

## <span data-ttu-id="71a05-135">Note</span><span class="sxs-lookup"><span data-stu-id="71a05-135">NOTES</span></span>

## <span data-ttu-id="71a05-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71a05-136">RELATED LINKS</span></span>

[<span data-ttu-id="71a05-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="71a05-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="71a05-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="71a05-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="71a05-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="71a05-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


