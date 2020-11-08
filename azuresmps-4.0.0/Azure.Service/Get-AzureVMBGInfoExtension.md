---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023490"
---
# <span data-ttu-id="edbf9-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="edbf9-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="edbf9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="edbf9-103">Ottiene l'estensione BGInfo applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="edbf9-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="edbf9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edbf9-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="edbf9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edbf9-105">DESCRIPTION</span></span>
<span data-ttu-id="edbf9-106">Il cmdlet **Get-AzureVMBGInfoExtension** Ottiene l'estensione BGInfo applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="edbf9-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="edbf9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edbf9-107">EXAMPLES</span></span>

### <span data-ttu-id="edbf9-108">Esempio 1: ottenere l'estensione BGInfo applicata in una macchina virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="edbf9-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="edbf9-109">Questo comando ottiene l'estensione BGInfo applicata a una macchina virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="edbf9-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="edbf9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edbf9-110">PARAMETERS</span></span>

### <span data-ttu-id="edbf9-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="edbf9-111">-InformationAction</span></span>
<span data-ttu-id="edbf9-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="edbf9-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="edbf9-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="edbf9-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="edbf9-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="edbf9-114">Continue</span></span>
- <span data-ttu-id="edbf9-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="edbf9-115">Ignore</span></span>
- <span data-ttu-id="edbf9-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="edbf9-116">Inquire</span></span>
- <span data-ttu-id="edbf9-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="edbf9-117">SilentlyContinue</span></span>
- <span data-ttu-id="edbf9-118">Stop</span><span class="sxs-lookup"><span data-stu-id="edbf9-118">Stop</span></span>
- <span data-ttu-id="edbf9-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="edbf9-119">Suspend</span></span>

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

### <span data-ttu-id="edbf9-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="edbf9-120">-InformationVariable</span></span>
<span data-ttu-id="edbf9-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="edbf9-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="edbf9-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="edbf9-122">-Profile</span></span>
<span data-ttu-id="edbf9-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edbf9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="edbf9-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="edbf9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="edbf9-125">-VM</span><span class="sxs-lookup"><span data-stu-id="edbf9-125">-VM</span></span>
<span data-ttu-id="edbf9-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="edbf9-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="edbf9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbf9-127">CommonParameters</span></span>
<span data-ttu-id="edbf9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbf9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbf9-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbf9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbf9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edbf9-130">INPUTS</span></span>

## <span data-ttu-id="edbf9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edbf9-131">OUTPUTS</span></span>

## <span data-ttu-id="edbf9-132">Note</span><span class="sxs-lookup"><span data-stu-id="edbf9-132">NOTES</span></span>

## <span data-ttu-id="edbf9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edbf9-133">RELATED LINKS</span></span>

[<span data-ttu-id="edbf9-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="edbf9-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="edbf9-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="edbf9-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


