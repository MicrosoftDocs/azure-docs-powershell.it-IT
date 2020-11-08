---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 93A8B8EC-4ED0-4C87-AF92-9A246ECEF4F0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1b516722b0555c84400c0c8f5acd7f1b5c43d9c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023468"
---
# <span data-ttu-id="6ecd2-101">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ecd2-101">Remove-AzureVMAccessExtension</span></span>

## <span data-ttu-id="6ecd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ecd2-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecd2-103">Rimuove l'estensione VMAccess applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-103">Removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6ecd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ecd2-104">SYNTAX</span></span>

```
Remove-AzureVMAccessExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6ecd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ecd2-105">DESCRIPTION</span></span>
<span data-ttu-id="6ecd2-106">Il cmdlet **Remove-AzureVMAccessExtension** rimuove l'estensione VMAccess applicata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-106">The **Remove-AzureVMAccessExtension** cmdlet removes the VMAccess extension applied on a virtual machine.</span></span>

## <span data-ttu-id="6ecd2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ecd2-107">EXAMPLES</span></span>

### <span data-ttu-id="6ecd2-108">Esempio 1: rimuovere un'estensione VMAccess da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="6ecd2-108">Example 1: Remove a VMAccess extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMAccessExtension -VM $VM;
```

<span data-ttu-id="6ecd2-109">Questo comando rimuove un'estensione VMAccess da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-109">This command removes a VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="6ecd2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ecd2-110">PARAMETERS</span></span>

### <span data-ttu-id="6ecd2-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6ecd2-111">-InformationAction</span></span>
<span data-ttu-id="6ecd2-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6ecd2-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ecd2-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ecd2-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="6ecd2-114">Continue</span></span>
- <span data-ttu-id="6ecd2-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="6ecd2-115">Ignore</span></span>
- <span data-ttu-id="6ecd2-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6ecd2-116">Inquire</span></span>
- <span data-ttu-id="6ecd2-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6ecd2-117">SilentlyContinue</span></span>
- <span data-ttu-id="6ecd2-118">Stop</span><span class="sxs-lookup"><span data-stu-id="6ecd2-118">Stop</span></span>
- <span data-ttu-id="6ecd2-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6ecd2-119">Suspend</span></span>

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

### <span data-ttu-id="6ecd2-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6ecd2-120">-InformationVariable</span></span>
<span data-ttu-id="6ecd2-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6ecd2-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="6ecd2-122">-Profile</span></span>
<span data-ttu-id="6ecd2-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ecd2-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6ecd2-125">-VM</span><span class="sxs-lookup"><span data-stu-id="6ecd2-125">-VM</span></span>
<span data-ttu-id="6ecd2-126">Specifica l'oggetto macchina virtuale persistente a cui questo cmdlet rimuove l'estensione VMAccess.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-126">Specifies the persistent virtual machine object that this cmdlet removes the VMAccess extension from.</span></span>

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

### <span data-ttu-id="6ecd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecd2-127">CommonParameters</span></span>
<span data-ttu-id="6ecd2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ecd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecd2-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ecd2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecd2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ecd2-130">INPUTS</span></span>

## <span data-ttu-id="6ecd2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ecd2-131">OUTPUTS</span></span>

## <span data-ttu-id="6ecd2-132">Note</span><span class="sxs-lookup"><span data-stu-id="6ecd2-132">NOTES</span></span>

## <span data-ttu-id="6ecd2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ecd2-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ecd2-134">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ecd2-134">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="6ecd2-135">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6ecd2-135">Set-AzureVMAccessExtension</span></span>](./Set-AzureVMAccessExtension.md)


