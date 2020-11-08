---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029928"
---
# <span data-ttu-id="0a0e6-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="0a0e6-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="0a0e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a0e6-102">SYNOPSIS</span></span>

## <span data-ttu-id="0a0e6-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a0e6-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0a0e6-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a0e6-104">DESCRIPTION</span></span>

## <span data-ttu-id="0a0e6-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a0e6-105">EXAMPLES</span></span>

### <span data-ttu-id="0a0e6-106">1:</span><span class="sxs-lookup"><span data-stu-id="0a0e6-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0a0e6-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a0e6-107">PARAMETERS</span></span>

### <span data-ttu-id="0a0e6-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0a0e6-108">-InformationAction</span></span>
<span data-ttu-id="0a0e6-109">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="0a0e6-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0a0e6-110">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a0e6-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a0e6-111">Continuare</span><span class="sxs-lookup"><span data-stu-id="0a0e6-111">Continue</span></span>
- <span data-ttu-id="0a0e6-112">Ignora</span><span class="sxs-lookup"><span data-stu-id="0a0e6-112">Ignore</span></span>
- <span data-ttu-id="0a0e6-113">Informarsi</span><span class="sxs-lookup"><span data-stu-id="0a0e6-113">Inquire</span></span>
- <span data-ttu-id="0a0e6-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0a0e6-114">SilentlyContinue</span></span>
- <span data-ttu-id="0a0e6-115">Stop</span><span class="sxs-lookup"><span data-stu-id="0a0e6-115">Stop</span></span>
- <span data-ttu-id="0a0e6-116">Sospensione</span><span class="sxs-lookup"><span data-stu-id="0a0e6-116">Suspend</span></span>

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

### <span data-ttu-id="0a0e6-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0a0e6-117">-InformationVariable</span></span>
<span data-ttu-id="0a0e6-118">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="0a0e6-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0a0e6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a0e6-119">-Name</span></span>
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

### <span data-ttu-id="0a0e6-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="0a0e6-120">-Profile</span></span>
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

### <span data-ttu-id="0a0e6-121">-VM</span><span class="sxs-lookup"><span data-stu-id="0a0e6-121">-VM</span></span>
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

### <span data-ttu-id="0a0e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0e6-122">CommonParameters</span></span>
<span data-ttu-id="0a0e6-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a0e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0e6-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0e6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0e6-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a0e6-125">INPUTS</span></span>

## <span data-ttu-id="0a0e6-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a0e6-126">OUTPUTS</span></span>

## <span data-ttu-id="0a0e6-127">Note</span><span class="sxs-lookup"><span data-stu-id="0a0e6-127">NOTES</span></span>

## <span data-ttu-id="0a0e6-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a0e6-128">RELATED LINKS</span></span>

[<span data-ttu-id="0a0e6-129">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="0a0e6-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="0a0e6-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="0a0e6-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="0a0e6-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="0a0e6-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


