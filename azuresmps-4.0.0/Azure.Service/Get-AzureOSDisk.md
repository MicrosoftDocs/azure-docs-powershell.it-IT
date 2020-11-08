---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A269A53-8FB2-4D4E-8FBB-A84BE658F75F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 002834bda663dda1c9ebe5f24bb0f1aa0007655c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029794"
---
# <span data-ttu-id="69e00-101">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="69e00-101">Get-AzureOSDisk</span></span>

## <span data-ttu-id="69e00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69e00-102">SYNOPSIS</span></span>
<span data-ttu-id="69e00-103">Ottiene il disco del sistema operativo di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="69e00-103">Gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="69e00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69e00-104">SYNTAX</span></span>

```
Get-AzureOSDisk -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="69e00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69e00-105">DESCRIPTION</span></span>
<span data-ttu-id="69e00-106">Il cmdlet **Get-AzureOSDisk** ottiene il disco del sistema operativo di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="69e00-106">The **Get-AzureOSDisk** cmdlet gets the operating system disk of an Azure virtual machine.</span></span>

## <span data-ttu-id="69e00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69e00-107">EXAMPLES</span></span>

### <span data-ttu-id="69e00-108">Esempio 1: ottenere un disco del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="69e00-108">Example 1: Get an operating system disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Get-AzureOSDisk
```

<span data-ttu-id="69e00-109">Questo comando ottiene la macchina virtuale denominata VirtualMachine02 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="69e00-109">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="69e00-110">Il comando passa la macchina virtuale al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="69e00-110">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="69e00-111">Il cmdlet corrente ottiene il disco del sistema operativo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="69e00-111">The current cmdlet gets the operating system disk of that virtual machine.</span></span>

## <span data-ttu-id="69e00-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69e00-112">PARAMETERS</span></span>

### <span data-ttu-id="69e00-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="69e00-113">-InformationAction</span></span>
<span data-ttu-id="69e00-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="69e00-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="69e00-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69e00-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69e00-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="69e00-116">Continue</span></span>
- <span data-ttu-id="69e00-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="69e00-117">Ignore</span></span>
- <span data-ttu-id="69e00-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="69e00-118">Inquire</span></span>
- <span data-ttu-id="69e00-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="69e00-119">SilentlyContinue</span></span>
- <span data-ttu-id="69e00-120">Stop</span><span class="sxs-lookup"><span data-stu-id="69e00-120">Stop</span></span>
- <span data-ttu-id="69e00-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="69e00-121">Suspend</span></span>

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

### <span data-ttu-id="69e00-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="69e00-122">-InformationVariable</span></span>
<span data-ttu-id="69e00-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="69e00-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="69e00-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="69e00-124">-Profile</span></span>
<span data-ttu-id="69e00-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69e00-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69e00-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="69e00-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69e00-127">-VM</span><span class="sxs-lookup"><span data-stu-id="69e00-127">-VM</span></span>
<span data-ttu-id="69e00-128">Specifica la macchina virtuale per cui questo cmdlet ottiene il disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69e00-128">Specifies the virtual machine for which this cmdlet gets the operating system disk.</span></span>
<span data-ttu-id="69e00-129">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="69e00-129">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="69e00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e00-130">CommonParameters</span></span>
<span data-ttu-id="69e00-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69e00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e00-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69e00-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e00-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69e00-133">INPUTS</span></span>

## <span data-ttu-id="69e00-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69e00-134">OUTPUTS</span></span>

## <span data-ttu-id="69e00-135">Note</span><span class="sxs-lookup"><span data-stu-id="69e00-135">NOTES</span></span>

## <span data-ttu-id="69e00-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69e00-136">RELATED LINKS</span></span>

[<span data-ttu-id="69e00-137">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="69e00-137">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="69e00-138">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="69e00-138">Set-AzureOSDisk</span></span>](./Set-AzureOSDisk.md)


