---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E1A3FF-E479-44CD-8147-15408DF3F79A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f8290b0e4f40305495b535b28b2a8f61d7911ed
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030005"
---
# <span data-ttu-id="c8c0a-101">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8c0a-101">Get-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="c8c0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c0a-103">Ottiene le impostazioni dell'estensione di diagnostica di Azure in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-103">Gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="c8c0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8c0a-104">SYNTAX</span></span>

```
Get-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8c0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c0a-106">Il cmdlet **Get-AzureVMDiagnosticsExtension** ottiene le impostazioni di Microsoft Azure Diagnostics Extension in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-106">The **Get-AzureVMDiagnosticsExtension** cmdlet gets the settings of the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="c8c0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8c0a-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c0a-108">Esempio 1: ottenere l'estensione di diagnostica applicata a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c8c0a-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVMDiagnosticsExtension -VM $VM
```

<span data-ttu-id="c8c0a-109">Questo comando consente di ottenere l'estensione di diagnostica applicata alla macchina virtuale specificata come archiviato nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-109">This command gets the diagnostics extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="c8c0a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8c0a-110">PARAMETERS</span></span>

### <span data-ttu-id="c8c0a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8c0a-111">-InformationAction</span></span>
<span data-ttu-id="c8c0a-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8c0a-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8c0a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8c0a-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="c8c0a-114">Continue</span></span>
- <span data-ttu-id="c8c0a-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="c8c0a-115">Ignore</span></span>
- <span data-ttu-id="c8c0a-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c8c0a-116">Inquire</span></span>
- <span data-ttu-id="c8c0a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8c0a-117">SilentlyContinue</span></span>
- <span data-ttu-id="c8c0a-118">Stop</span><span class="sxs-lookup"><span data-stu-id="c8c0a-118">Stop</span></span>
- <span data-ttu-id="c8c0a-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c8c0a-119">Suspend</span></span>

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

### <span data-ttu-id="c8c0a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8c0a-120">-InformationVariable</span></span>
<span data-ttu-id="c8c0a-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8c0a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="c8c0a-122">-Profile</span></span>
<span data-ttu-id="c8c0a-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8c0a-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8c0a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="c8c0a-125">-VM</span></span>
<span data-ttu-id="c8c0a-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="c8c0a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c0a-127">CommonParameters</span></span>
<span data-ttu-id="c8c0a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c0a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c0a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c0a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c0a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8c0a-130">INPUTS</span></span>

## <span data-ttu-id="c8c0a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8c0a-131">OUTPUTS</span></span>

## <span data-ttu-id="c8c0a-132">Note</span><span class="sxs-lookup"><span data-stu-id="c8c0a-132">NOTES</span></span>

## <span data-ttu-id="c8c0a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8c0a-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8c0a-134">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8c0a-134">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="c8c0a-135">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c8c0a-135">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)


