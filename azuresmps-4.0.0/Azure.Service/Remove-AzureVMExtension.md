---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023459"
---
# <span data-ttu-id="addc4-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="addc4-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="addc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="addc4-102">SYNOPSIS</span></span>
<span data-ttu-id="addc4-103">Rimuove le estensioni delle risorse da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="addc4-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="addc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="addc4-104">SYNTAX</span></span>

### <span data-ttu-id="addc4-105">RemoveByExtensionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="addc4-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="addc4-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="addc4-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="addc4-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="addc4-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="addc4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="addc4-108">DESCRIPTION</span></span>
<span data-ttu-id="addc4-109">Il cmdlet **Remove-AzureVMExtension** rimuove le estensioni delle risorse da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="addc4-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="addc4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="addc4-110">EXAMPLES</span></span>

### <span data-ttu-id="addc4-111">Esempio 1: rimuovere un'estensione usando un nome e un autore specifici</span><span class="sxs-lookup"><span data-stu-id="addc4-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="addc4-112">Questo comando consente di rimuovere un'estensione con il nome e l'editore specificati.</span><span class="sxs-lookup"><span data-stu-id="addc4-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="addc4-113">Esempio 2: rimuovere tutte le estensioni da una macchina virtuale specifica</span><span class="sxs-lookup"><span data-stu-id="addc4-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="addc4-114">Questo comando rimuove tutte le estensioni dalla macchina virtuale specificata come archiviate nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="addc4-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="addc4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="addc4-115">PARAMETERS</span></span>

### <span data-ttu-id="addc4-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="addc4-116">-ExtensionName</span></span>
<span data-ttu-id="addc4-117">Specifica il nome dell'estensione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="addc4-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="addc4-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="addc4-118">-InformationAction</span></span>
<span data-ttu-id="addc4-119">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="addc4-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="addc4-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="addc4-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="addc4-121">Continuare</span><span class="sxs-lookup"><span data-stu-id="addc4-121">Continue</span></span>
- <span data-ttu-id="addc4-122">Ignora</span><span class="sxs-lookup"><span data-stu-id="addc4-122">Ignore</span></span>
- <span data-ttu-id="addc4-123">Informarsi</span><span class="sxs-lookup"><span data-stu-id="addc4-123">Inquire</span></span>
- <span data-ttu-id="addc4-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="addc4-124">SilentlyContinue</span></span>
- <span data-ttu-id="addc4-125">Stop</span><span class="sxs-lookup"><span data-stu-id="addc4-125">Stop</span></span>
- <span data-ttu-id="addc4-126">Sospensione</span><span class="sxs-lookup"><span data-stu-id="addc4-126">Suspend</span></span>

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

### <span data-ttu-id="addc4-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="addc4-127">-InformationVariable</span></span>
<span data-ttu-id="addc4-128">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="addc4-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="addc4-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="addc4-129">-Profile</span></span>
<span data-ttu-id="addc4-130">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="addc4-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="addc4-131">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="addc4-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="addc4-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="addc4-132">-Publisher</span></span>
<span data-ttu-id="addc4-133">Specifica l'estensione Publisher.</span><span class="sxs-lookup"><span data-stu-id="addc4-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="addc4-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="addc4-134">-ReferenceName</span></span>
<span data-ttu-id="addc4-135">Specifica il nome di riferimento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="addc4-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="addc4-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="addc4-136">-RemoveAll</span></span>
<span data-ttu-id="addc4-137">Indica che questo cmdlet rimuove tutte le estensioni delle risorse dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="addc4-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="addc4-138">-VM</span><span class="sxs-lookup"><span data-stu-id="addc4-138">-VM</span></span>
<span data-ttu-id="addc4-139">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="addc4-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="addc4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addc4-140">CommonParameters</span></span>
<span data-ttu-id="addc4-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addc4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addc4-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addc4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addc4-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="addc4-143">INPUTS</span></span>

## <span data-ttu-id="addc4-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="addc4-144">OUTPUTS</span></span>

## <span data-ttu-id="addc4-145">Note</span><span class="sxs-lookup"><span data-stu-id="addc4-145">NOTES</span></span>

## <span data-ttu-id="addc4-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="addc4-146">RELATED LINKS</span></span>

[<span data-ttu-id="addc4-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="addc4-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="addc4-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="addc4-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


