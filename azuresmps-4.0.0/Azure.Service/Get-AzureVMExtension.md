---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029995"
---
# <span data-ttu-id="b9e0f-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="b9e0f-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="b9e0f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e0f-103">Ottiene le estensioni delle risorse applicate alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="b9e0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9e0f-104">SYNTAX</span></span>

### <span data-ttu-id="b9e0f-105">ListByReferenceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9e0f-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9e0f-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="b9e0f-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9e0f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9e0f-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e0f-108">Il cmdlet **Get-AzureVMExtension** ottiene le estensioni delle risorse applicate alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="b9e0f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9e0f-109">EXAMPLES</span></span>

### <span data-ttu-id="b9e0f-110">Esempio 1: ottenere le estensioni delle risorse applicate a una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b9e0f-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="b9e0f-111">Questo comando consente di ottenere le estensioni delle risorse applicate alla macchina virtuale specificata come archiviate nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="b9e0f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9e0f-112">PARAMETERS</span></span>

### <span data-ttu-id="b9e0f-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b9e0f-113">-ExtensionName</span></span>
<span data-ttu-id="b9e0f-114">Specifica il nome dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e0f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b9e0f-115">-InformationAction</span></span>
<span data-ttu-id="b9e0f-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b9e0f-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9e0f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9e0f-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="b9e0f-118">Continue</span></span>
- <span data-ttu-id="b9e0f-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="b9e0f-119">Ignore</span></span>
- <span data-ttu-id="b9e0f-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b9e0f-120">Inquire</span></span>
- <span data-ttu-id="b9e0f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b9e0f-121">SilentlyContinue</span></span>
- <span data-ttu-id="b9e0f-122">Stop</span><span class="sxs-lookup"><span data-stu-id="b9e0f-122">Stop</span></span>
- <span data-ttu-id="b9e0f-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b9e0f-123">Suspend</span></span>

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

### <span data-ttu-id="b9e0f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b9e0f-124">-InformationVariable</span></span>
<span data-ttu-id="b9e0f-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b9e0f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="b9e0f-126">-Profile</span></span>
<span data-ttu-id="b9e0f-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b9e0f-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b9e0f-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b9e0f-129">-Publisher</span></span>
<span data-ttu-id="b9e0f-130">Specifica l'editore dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e0f-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="b9e0f-131">-ReferenceName</span></span>
<span data-ttu-id="b9e0f-132">Specifica il nome di riferimento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e0f-133">-Versione</span><span class="sxs-lookup"><span data-stu-id="b9e0f-133">-Version</span></span>
<span data-ttu-id="b9e0f-134">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e0f-135">-VM</span><span class="sxs-lookup"><span data-stu-id="b9e0f-135">-VM</span></span>
<span data-ttu-id="b9e0f-136">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b9e0f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e0f-137">CommonParameters</span></span>
<span data-ttu-id="b9e0f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e0f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e0f-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9e0f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e0f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9e0f-140">INPUTS</span></span>

## <span data-ttu-id="b9e0f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9e0f-141">OUTPUTS</span></span>

## <span data-ttu-id="b9e0f-142">Note</span><span class="sxs-lookup"><span data-stu-id="b9e0f-142">NOTES</span></span>

## <span data-ttu-id="b9e0f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9e0f-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9e0f-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="b9e0f-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="b9e0f-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="b9e0f-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


