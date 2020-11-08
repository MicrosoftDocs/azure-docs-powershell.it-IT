---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AB4700D-571B-497A-9742-2654844553B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: b46f15053639ec295d958766dac846d4f95e0368
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029613"
---
# <span data-ttu-id="dfa89-101">Remove-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="dfa89-101">Remove-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="dfa89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfa89-102">SYNOPSIS</span></span>

## <span data-ttu-id="dfa89-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfa89-103">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupConfig [[-NetworkSecurityGroupName] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfa89-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfa89-104">DESCRIPTION</span></span>

## <span data-ttu-id="dfa89-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfa89-105">EXAMPLES</span></span>

### <span data-ttu-id="dfa89-106">1:</span><span class="sxs-lookup"><span data-stu-id="dfa89-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="dfa89-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfa89-107">PARAMETERS</span></span>

### <span data-ttu-id="dfa89-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dfa89-108">-InformationAction</span></span>
<span data-ttu-id="dfa89-109">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="dfa89-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dfa89-110">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfa89-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfa89-111">Continuare</span><span class="sxs-lookup"><span data-stu-id="dfa89-111">Continue</span></span>
- <span data-ttu-id="dfa89-112">Ignora</span><span class="sxs-lookup"><span data-stu-id="dfa89-112">Ignore</span></span>
- <span data-ttu-id="dfa89-113">Informarsi</span><span class="sxs-lookup"><span data-stu-id="dfa89-113">Inquire</span></span>
- <span data-ttu-id="dfa89-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dfa89-114">SilentlyContinue</span></span>
- <span data-ttu-id="dfa89-115">Stop</span><span class="sxs-lookup"><span data-stu-id="dfa89-115">Stop</span></span>
- <span data-ttu-id="dfa89-116">Sospensione</span><span class="sxs-lookup"><span data-stu-id="dfa89-116">Suspend</span></span>

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

### <span data-ttu-id="dfa89-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dfa89-117">-InformationVariable</span></span>
<span data-ttu-id="dfa89-118">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="dfa89-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dfa89-119">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa89-119">-NetworkSecurityGroupName</span></span>
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

### <span data-ttu-id="dfa89-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="dfa89-120">-Profile</span></span>
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

### <span data-ttu-id="dfa89-121">-VM</span><span class="sxs-lookup"><span data-stu-id="dfa89-121">-VM</span></span>
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

### <span data-ttu-id="dfa89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa89-122">CommonParameters</span></span>
<span data-ttu-id="dfa89-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa89-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa89-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa89-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfa89-125">INPUTS</span></span>

## <span data-ttu-id="dfa89-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfa89-126">OUTPUTS</span></span>

## <span data-ttu-id="dfa89-127">Note</span><span class="sxs-lookup"><span data-stu-id="dfa89-127">NOTES</span></span>

## <span data-ttu-id="dfa89-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfa89-128">RELATED LINKS</span></span>

[<span data-ttu-id="dfa89-129">Set-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="dfa89-129">Set-AzureNetworkSecurityGroupConfig</span></span>](./Set-AzureNetworkSecurityGroupConfig.md)


