---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023462"
---
# <span data-ttu-id="05c4d-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05c4d-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="05c4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="05c4d-103">Rimuove l'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05c4d-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="05c4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05c4d-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="05c4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="05c4d-106">Il cmdlet **Remove-AzureVMDiagnosticsExtension** rimuove un'estensione di diagnostica Microsoft Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05c4d-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="05c4d-107">È necessario passare l'output di questo cmdlet al cmdlet **Update-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="05c4d-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="05c4d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05c4d-108">EXAMPLES</span></span>

### <span data-ttu-id="05c4d-109">Esempio 1: rimuovere l'estensione di diagnostica di Azure da una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="05c4d-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="05c4d-110">Questo comando rimuove l'estensione di diagnostica di Azure da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05c4d-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="05c4d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05c4d-111">PARAMETERS</span></span>

### <span data-ttu-id="05c4d-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="05c4d-112">-InformationAction</span></span>
<span data-ttu-id="05c4d-113">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="05c4d-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="05c4d-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="05c4d-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05c4d-115">Continuare</span><span class="sxs-lookup"><span data-stu-id="05c4d-115">Continue</span></span>
- <span data-ttu-id="05c4d-116">Ignora</span><span class="sxs-lookup"><span data-stu-id="05c4d-116">Ignore</span></span>
- <span data-ttu-id="05c4d-117">Informarsi</span><span class="sxs-lookup"><span data-stu-id="05c4d-117">Inquire</span></span>
- <span data-ttu-id="05c4d-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="05c4d-118">SilentlyContinue</span></span>
- <span data-ttu-id="05c4d-119">Stop</span><span class="sxs-lookup"><span data-stu-id="05c4d-119">Stop</span></span>
- <span data-ttu-id="05c4d-120">Sospensione</span><span class="sxs-lookup"><span data-stu-id="05c4d-120">Suspend</span></span>

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

### <span data-ttu-id="05c4d-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="05c4d-121">-InformationVariable</span></span>
<span data-ttu-id="05c4d-122">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="05c4d-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="05c4d-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="05c4d-123">-Profile</span></span>
<span data-ttu-id="05c4d-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05c4d-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05c4d-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="05c4d-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05c4d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="05c4d-126">-VM</span></span>
<span data-ttu-id="05c4d-127">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="05c4d-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="05c4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c4d-128">CommonParameters</span></span>
<span data-ttu-id="05c4d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05c4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c4d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05c4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c4d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05c4d-131">INPUTS</span></span>

## <span data-ttu-id="05c4d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05c4d-132">OUTPUTS</span></span>

## <span data-ttu-id="05c4d-133">Note</span><span class="sxs-lookup"><span data-stu-id="05c4d-133">NOTES</span></span>

## <span data-ttu-id="05c4d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05c4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="05c4d-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05c4d-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="05c4d-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="05c4d-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="05c4d-137">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="05c4d-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


