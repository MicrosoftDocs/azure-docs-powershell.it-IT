---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FE31EE5C-830F-4B5E-82DB-C881032EF05C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c1160478da2c84f2d792ab570b05d544f4537bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029856"
---
# <span data-ttu-id="d1b12-101">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d1b12-101">Add-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="d1b12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1b12-102">SYNOPSIS</span></span>

## <span data-ttu-id="d1b12-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1b12-103">SYNTAX</span></span>

```
Add-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d1b12-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1b12-104">DESCRIPTION</span></span>

## <span data-ttu-id="d1b12-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1b12-105">EXAMPLES</span></span>

### <span data-ttu-id="d1b12-106">1:</span><span class="sxs-lookup"><span data-stu-id="d1b12-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d1b12-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1b12-107">PARAMETERS</span></span>

### <span data-ttu-id="d1b12-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d1b12-108">-InformationAction</span></span>
<span data-ttu-id="d1b12-109">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d1b12-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d1b12-110">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1b12-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1b12-111">Continuare</span><span class="sxs-lookup"><span data-stu-id="d1b12-111">Continue</span></span>
- <span data-ttu-id="d1b12-112">Ignora</span><span class="sxs-lookup"><span data-stu-id="d1b12-112">Ignore</span></span>
- <span data-ttu-id="d1b12-113">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d1b12-113">Inquire</span></span>
- <span data-ttu-id="d1b12-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d1b12-114">SilentlyContinue</span></span>
- <span data-ttu-id="d1b12-115">Stop</span><span class="sxs-lookup"><span data-stu-id="d1b12-115">Stop</span></span>
- <span data-ttu-id="d1b12-116">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d1b12-116">Suspend</span></span>

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

### <span data-ttu-id="d1b12-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d1b12-117">-InformationVariable</span></span>
<span data-ttu-id="d1b12-118">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d1b12-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d1b12-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="d1b12-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b12-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1b12-120">-Name</span></span>
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

### <span data-ttu-id="d1b12-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d1b12-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b12-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="d1b12-122">-Profile</span></span>
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

### <span data-ttu-id="d1b12-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="d1b12-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b12-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d1b12-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1b12-125">-VM</span><span class="sxs-lookup"><span data-stu-id="d1b12-125">-VM</span></span>
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

### <span data-ttu-id="d1b12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b12-126">CommonParameters</span></span>
<span data-ttu-id="d1b12-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b12-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b12-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b12-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1b12-129">INPUTS</span></span>

## <span data-ttu-id="d1b12-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1b12-130">OUTPUTS</span></span>

## <span data-ttu-id="d1b12-131">Note</span><span class="sxs-lookup"><span data-stu-id="d1b12-131">NOTES</span></span>

## <span data-ttu-id="d1b12-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1b12-132">RELATED LINKS</span></span>

[<span data-ttu-id="d1b12-133">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d1b12-133">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="d1b12-134">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d1b12-134">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="d1b12-135">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="d1b12-135">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


