---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023466"
---
# <span data-ttu-id="05e2a-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="05e2a-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="05e2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="05e2a-103">Rimuove l'estensione BGInfo applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05e2a-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="05e2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05e2a-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="05e2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05e2a-105">DESCRIPTION</span></span>
<span data-ttu-id="05e2a-106">Il cmdlet **Remove-AzureVMBGInfoExtension** rimuove l'estensione BGInfo applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05e2a-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="05e2a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05e2a-107">EXAMPLES</span></span>

### <span data-ttu-id="05e2a-108">Esempio 1: rimuovere l'estensione BGInfo in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="05e2a-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="05e2a-109">Questo comando rimuove l'estensione BGInfo applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05e2a-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="05e2a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05e2a-110">PARAMETERS</span></span>

### <span data-ttu-id="05e2a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="05e2a-111">-InformationAction</span></span>
<span data-ttu-id="05e2a-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="05e2a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="05e2a-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="05e2a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05e2a-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="05e2a-114">Continue</span></span>
- <span data-ttu-id="05e2a-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="05e2a-115">Ignore</span></span>
- <span data-ttu-id="05e2a-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="05e2a-116">Inquire</span></span>
- <span data-ttu-id="05e2a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="05e2a-117">SilentlyContinue</span></span>
- <span data-ttu-id="05e2a-118">Stop</span><span class="sxs-lookup"><span data-stu-id="05e2a-118">Stop</span></span>
- <span data-ttu-id="05e2a-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="05e2a-119">Suspend</span></span>

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

### <span data-ttu-id="05e2a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="05e2a-120">-InformationVariable</span></span>
<span data-ttu-id="05e2a-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="05e2a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="05e2a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="05e2a-122">-Profile</span></span>
<span data-ttu-id="05e2a-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e2a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05e2a-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="05e2a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05e2a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="05e2a-125">-VM</span></span>
<span data-ttu-id="05e2a-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="05e2a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="05e2a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e2a-127">CommonParameters</span></span>
<span data-ttu-id="05e2a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e2a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e2a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e2a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e2a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05e2a-130">INPUTS</span></span>

## <span data-ttu-id="05e2a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05e2a-131">OUTPUTS</span></span>

## <span data-ttu-id="05e2a-132">Note</span><span class="sxs-lookup"><span data-stu-id="05e2a-132">NOTES</span></span>

## <span data-ttu-id="05e2a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05e2a-133">RELATED LINKS</span></span>

[<span data-ttu-id="05e2a-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="05e2a-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="05e2a-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="05e2a-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)


