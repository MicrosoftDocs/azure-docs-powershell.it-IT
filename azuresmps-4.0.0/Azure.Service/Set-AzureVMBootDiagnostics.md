---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023751"
---
# <span data-ttu-id="0bafd-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0bafd-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="0bafd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bafd-102">SYNOPSIS</span></span>

## <span data-ttu-id="0bafd-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bafd-103">SYNTAX</span></span>

### <span data-ttu-id="0bafd-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0bafd-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0bafd-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0bafd-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0bafd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bafd-106">DESCRIPTION</span></span>

## <span data-ttu-id="0bafd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bafd-107">EXAMPLES</span></span>

### <span data-ttu-id="0bafd-108">1:</span><span class="sxs-lookup"><span data-stu-id="0bafd-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0bafd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bafd-109">PARAMETERS</span></span>

### <span data-ttu-id="0bafd-110">-Disable</span><span class="sxs-lookup"><span data-stu-id="0bafd-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bafd-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="0bafd-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bafd-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0bafd-112">-InformationAction</span></span>
<span data-ttu-id="0bafd-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="0bafd-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0bafd-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0bafd-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0bafd-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="0bafd-115">Continue</span></span>
- <span data-ttu-id="0bafd-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="0bafd-116">Ignore</span></span>
- <span data-ttu-id="0bafd-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="0bafd-117">Inquire</span></span>
- <span data-ttu-id="0bafd-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0bafd-118">SilentlyContinue</span></span>
- <span data-ttu-id="0bafd-119">Stop</span><span class="sxs-lookup"><span data-stu-id="0bafd-119">Stop</span></span>
- <span data-ttu-id="0bafd-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="0bafd-120">Suspend</span></span>

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

### <span data-ttu-id="0bafd-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0bafd-121">-InformationVariable</span></span>
<span data-ttu-id="0bafd-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="0bafd-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0bafd-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="0bafd-123">-Profile</span></span>
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

### <span data-ttu-id="0bafd-124">-VM</span><span class="sxs-lookup"><span data-stu-id="0bafd-124">-VM</span></span>
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

### <span data-ttu-id="0bafd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bafd-125">CommonParameters</span></span>
<span data-ttu-id="0bafd-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bafd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bafd-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bafd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bafd-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bafd-128">INPUTS</span></span>

## <span data-ttu-id="0bafd-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bafd-129">OUTPUTS</span></span>

## <span data-ttu-id="0bafd-130">Note</span><span class="sxs-lookup"><span data-stu-id="0bafd-130">NOTES</span></span>

## <span data-ttu-id="0bafd-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bafd-131">RELATED LINKS</span></span>

