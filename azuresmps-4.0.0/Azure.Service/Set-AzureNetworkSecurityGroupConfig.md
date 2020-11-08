---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8E64309-7AF6-4439-841E-922B11C072AA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15dd195b86e70ad0a95484417d8cf87b0e544920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023714"
---
# <span data-ttu-id="96b28-101">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="96b28-101">Set-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="96b28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96b28-102">SYNOPSIS</span></span>

## <span data-ttu-id="96b28-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96b28-103">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupConfig [-NetworkSecurityGroupName] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="96b28-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96b28-104">DESCRIPTION</span></span>

## <span data-ttu-id="96b28-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96b28-105">EXAMPLES</span></span>

### <span data-ttu-id="96b28-106">1:</span><span class="sxs-lookup"><span data-stu-id="96b28-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="96b28-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96b28-107">PARAMETERS</span></span>

### <span data-ttu-id="96b28-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="96b28-108">-InformationAction</span></span>
<span data-ttu-id="96b28-109">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="96b28-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="96b28-110">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="96b28-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="96b28-111">Continuare</span><span class="sxs-lookup"><span data-stu-id="96b28-111">Continue</span></span>
- <span data-ttu-id="96b28-112">Ignora</span><span class="sxs-lookup"><span data-stu-id="96b28-112">Ignore</span></span>
- <span data-ttu-id="96b28-113">Informarsi</span><span class="sxs-lookup"><span data-stu-id="96b28-113">Inquire</span></span>
- <span data-ttu-id="96b28-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="96b28-114">SilentlyContinue</span></span>
- <span data-ttu-id="96b28-115">Stop</span><span class="sxs-lookup"><span data-stu-id="96b28-115">Stop</span></span>
- <span data-ttu-id="96b28-116">Sospensione</span><span class="sxs-lookup"><span data-stu-id="96b28-116">Suspend</span></span>

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

### <span data-ttu-id="96b28-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="96b28-117">-InformationVariable</span></span>
<span data-ttu-id="96b28-118">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="96b28-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="96b28-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="96b28-119">-NetworkSecurityGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b28-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="96b28-120">-Profile</span></span>
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

### <span data-ttu-id="96b28-121">-VM</span><span class="sxs-lookup"><span data-stu-id="96b28-121">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b28-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b28-122">CommonParameters</span></span>
<span data-ttu-id="96b28-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96b28-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b28-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96b28-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b28-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96b28-125">INPUTS</span></span>

## <span data-ttu-id="96b28-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96b28-126">OUTPUTS</span></span>

## <span data-ttu-id="96b28-127">Note</span><span class="sxs-lookup"><span data-stu-id="96b28-127">NOTES</span></span>

## <span data-ttu-id="96b28-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96b28-128">RELATED LINKS</span></span>

[<span data-ttu-id="96b28-129">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="96b28-129">Remove-AzureNetworkSecurityGroupConfig</span></span>](./Remove-AzureNetworkSecurityGroupConfig.md)


