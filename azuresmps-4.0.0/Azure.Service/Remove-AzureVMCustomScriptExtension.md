---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029910"
---
# <span data-ttu-id="88902-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="88902-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="88902-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88902-102">SYNOPSIS</span></span>
<span data-ttu-id="88902-103">Rimuove l'estensione di script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88902-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="88902-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88902-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="88902-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88902-105">DESCRIPTION</span></span>
<span data-ttu-id="88902-106">Il cmdlet **Remove-AzureVMCustomScriptExtension** rimuove l'estensione di script personalizzata da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="88902-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="88902-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88902-107">EXAMPLES</span></span>

### <span data-ttu-id="88902-108">Esempio 1: rimuovere un'estensione di script personalizzata della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="88902-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="88902-109">Questo comando rimuove l'estensione di script personalizzata di Azure Virtual Machine dalla macchina virtuale specificata come archiviato nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="88902-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="88902-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88902-110">PARAMETERS</span></span>

### <span data-ttu-id="88902-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="88902-111">-InformationAction</span></span>
<span data-ttu-id="88902-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="88902-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="88902-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="88902-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88902-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="88902-114">Continue</span></span>
- <span data-ttu-id="88902-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="88902-115">Ignore</span></span>
- <span data-ttu-id="88902-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="88902-116">Inquire</span></span>
- <span data-ttu-id="88902-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="88902-117">SilentlyContinue</span></span>
- <span data-ttu-id="88902-118">Stop</span><span class="sxs-lookup"><span data-stu-id="88902-118">Stop</span></span>
- <span data-ttu-id="88902-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="88902-119">Suspend</span></span>

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

### <span data-ttu-id="88902-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="88902-120">-InformationVariable</span></span>
<span data-ttu-id="88902-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="88902-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="88902-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="88902-122">-Profile</span></span>
<span data-ttu-id="88902-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88902-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88902-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="88902-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88902-125">-VM</span><span class="sxs-lookup"><span data-stu-id="88902-125">-VM</span></span>
<span data-ttu-id="88902-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="88902-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="88902-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88902-127">CommonParameters</span></span>
<span data-ttu-id="88902-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88902-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88902-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88902-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88902-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88902-130">INPUTS</span></span>

## <span data-ttu-id="88902-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88902-131">OUTPUTS</span></span>

## <span data-ttu-id="88902-132">Note</span><span class="sxs-lookup"><span data-stu-id="88902-132">NOTES</span></span>

## <span data-ttu-id="88902-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88902-133">RELATED LINKS</span></span>

[<span data-ttu-id="88902-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="88902-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="88902-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="88902-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


