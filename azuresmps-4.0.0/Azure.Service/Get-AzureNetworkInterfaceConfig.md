---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030046"
---
# <span data-ttu-id="f3b26-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="f3b26-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="f3b26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3b26-102">SYNOPSIS</span></span>

## <span data-ttu-id="f3b26-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3b26-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f3b26-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3b26-104">DESCRIPTION</span></span>

## <span data-ttu-id="f3b26-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3b26-105">EXAMPLES</span></span>

### <span data-ttu-id="f3b26-106">1:</span><span class="sxs-lookup"><span data-stu-id="f3b26-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f3b26-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3b26-107">PARAMETERS</span></span>

### <span data-ttu-id="f3b26-108">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f3b26-108">-InformationAction</span></span>
<span data-ttu-id="f3b26-109">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="f3b26-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f3b26-110">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3b26-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3b26-111">Continuare</span><span class="sxs-lookup"><span data-stu-id="f3b26-111">Continue</span></span>
- <span data-ttu-id="f3b26-112">Ignora</span><span class="sxs-lookup"><span data-stu-id="f3b26-112">Ignore</span></span>
- <span data-ttu-id="f3b26-113">Informarsi</span><span class="sxs-lookup"><span data-stu-id="f3b26-113">Inquire</span></span>
- <span data-ttu-id="f3b26-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f3b26-114">SilentlyContinue</span></span>
- <span data-ttu-id="f3b26-115">Stop</span><span class="sxs-lookup"><span data-stu-id="f3b26-115">Stop</span></span>
- <span data-ttu-id="f3b26-116">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f3b26-116">Suspend</span></span>

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

### <span data-ttu-id="f3b26-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f3b26-117">-InformationVariable</span></span>
<span data-ttu-id="f3b26-118">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="f3b26-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f3b26-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3b26-119">-Name</span></span>
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

### <span data-ttu-id="f3b26-120">-VM</span><span class="sxs-lookup"><span data-stu-id="f3b26-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b26-121">CommonParameters</span></span>
<span data-ttu-id="f3b26-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b26-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b26-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b26-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3b26-124">INPUTS</span></span>

## <span data-ttu-id="f3b26-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3b26-125">OUTPUTS</span></span>

## <span data-ttu-id="f3b26-126">Note</span><span class="sxs-lookup"><span data-stu-id="f3b26-126">NOTES</span></span>

## <span data-ttu-id="f3b26-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3b26-127">RELATED LINKS</span></span>

[<span data-ttu-id="f3b26-128">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="f3b26-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="f3b26-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="f3b26-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="f3b26-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="f3b26-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


