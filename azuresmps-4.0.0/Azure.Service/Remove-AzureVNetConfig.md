---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023450"
---
# <span data-ttu-id="ea684-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="ea684-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="ea684-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea684-102">SYNOPSIS</span></span>
<span data-ttu-id="ea684-103">Elimina la configurazione di rete dall'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="ea684-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="ea684-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea684-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea684-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea684-105">DESCRIPTION</span></span>
<span data-ttu-id="ea684-106">Il cmdlet **Remove-AzureVNetConfig** consente di rimuovere tutte le impostazioni di rete virtuale dall'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="ea684-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="ea684-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea684-107">EXAMPLES</span></span>

### <span data-ttu-id="ea684-108">Esempio 1: rimuovere una configurazione di rete virtuale dall'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="ea684-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="ea684-109">Questo comando rimuove la configurazione di rete virtuale dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ea684-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="ea684-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea684-110">PARAMETERS</span></span>

### <span data-ttu-id="ea684-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea684-111">-InformationAction</span></span>
<span data-ttu-id="ea684-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="ea684-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea684-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea684-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea684-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="ea684-114">Continue</span></span>
- <span data-ttu-id="ea684-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="ea684-115">Ignore</span></span>
- <span data-ttu-id="ea684-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="ea684-116">Inquire</span></span>
- <span data-ttu-id="ea684-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea684-117">SilentlyContinue</span></span>
- <span data-ttu-id="ea684-118">Stop</span><span class="sxs-lookup"><span data-stu-id="ea684-118">Stop</span></span>
- <span data-ttu-id="ea684-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="ea684-119">Suspend</span></span>

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

### <span data-ttu-id="ea684-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea684-120">-InformationVariable</span></span>
<span data-ttu-id="ea684-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="ea684-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea684-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="ea684-122">-Profile</span></span>
<span data-ttu-id="ea684-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea684-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea684-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ea684-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea684-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea684-125">CommonParameters</span></span>
<span data-ttu-id="ea684-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea684-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea684-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea684-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea684-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea684-128">INPUTS</span></span>

## <span data-ttu-id="ea684-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea684-129">OUTPUTS</span></span>

## <span data-ttu-id="ea684-130">Note</span><span class="sxs-lookup"><span data-stu-id="ea684-130">NOTES</span></span>

## <span data-ttu-id="ea684-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea684-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea684-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="ea684-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="ea684-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="ea684-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="ea684-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="ea684-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


