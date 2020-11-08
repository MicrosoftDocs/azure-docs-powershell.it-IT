---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029750"
---
# <span data-ttu-id="93563-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="93563-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="93563-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93563-102">SYNOPSIS</span></span>
<span data-ttu-id="93563-103">Ottiene la configurazione di rete virtuale Azure dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="93563-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="93563-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93563-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="93563-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93563-105">DESCRIPTION</span></span>
<span data-ttu-id="93563-106">Il cmdlet **Get-AzureVNetConfig** recupera la configurazione di rete virtuale dell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="93563-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="93563-107">Se viene specificato il parametro *ExportToFile* , viene creato un file di configurazione della rete.</span><span class="sxs-lookup"><span data-stu-id="93563-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="93563-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93563-108">EXAMPLES</span></span>

### <span data-ttu-id="93563-109">Esempio 1: ottenere la configurazione di rete virtuale di un abbonamento a Azure corrente</span><span class="sxs-lookup"><span data-stu-id="93563-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="93563-110">Questo comando consente di ottenere la configurazione di rete virtuale dell'abbonamento Azure corrente e di visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="93563-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="93563-111">Esempio 2: ottenere la configurazione di rete virtuale dell'abbonamento Azure corrente e salvarlo in un file locale</span><span class="sxs-lookup"><span data-stu-id="93563-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="93563-112">Questo comando consente di ottenere la configurazione di rete virtuale dell'abbonamento Azure corrente e quindi di salvarlo in un file locale.</span><span class="sxs-lookup"><span data-stu-id="93563-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="93563-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93563-113">PARAMETERS</span></span>

### <span data-ttu-id="93563-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="93563-114">-ExportToFile</span></span>
<span data-ttu-id="93563-115">Specifica il percorso e il nome file di un file di configurazione di rete da creare dalle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="93563-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93563-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="93563-116">-InformationAction</span></span>
<span data-ttu-id="93563-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="93563-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="93563-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="93563-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93563-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="93563-119">Continue</span></span>
- <span data-ttu-id="93563-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="93563-120">Ignore</span></span>
- <span data-ttu-id="93563-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="93563-121">Inquire</span></span>
- <span data-ttu-id="93563-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="93563-122">SilentlyContinue</span></span>
- <span data-ttu-id="93563-123">Stop</span><span class="sxs-lookup"><span data-stu-id="93563-123">Stop</span></span>
- <span data-ttu-id="93563-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="93563-124">Suspend</span></span>

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

### <span data-ttu-id="93563-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="93563-125">-InformationVariable</span></span>
<span data-ttu-id="93563-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="93563-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="93563-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="93563-127">-Profile</span></span>
<span data-ttu-id="93563-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93563-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93563-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="93563-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93563-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93563-130">CommonParameters</span></span>
<span data-ttu-id="93563-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93563-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93563-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93563-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93563-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93563-133">INPUTS</span></span>

## <span data-ttu-id="93563-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93563-134">OUTPUTS</span></span>

## <span data-ttu-id="93563-135">Note</span><span class="sxs-lookup"><span data-stu-id="93563-135">NOTES</span></span>

## <span data-ttu-id="93563-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93563-136">RELATED LINKS</span></span>

[<span data-ttu-id="93563-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="93563-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="93563-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="93563-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="93563-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="93563-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


