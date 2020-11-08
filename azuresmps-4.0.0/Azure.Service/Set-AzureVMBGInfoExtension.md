---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029505"
---
# <span data-ttu-id="20bf1-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="20bf1-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="20bf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="20bf1-103">Imposta l'estensione BGInfo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="20bf1-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="20bf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20bf1-104">SYNTAX</span></span>

### <span data-ttu-id="20bf1-105">SetBGInfoExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20bf1-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="20bf1-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="20bf1-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="20bf1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20bf1-107">DESCRIPTION</span></span>
<span data-ttu-id="20bf1-108">Il cmdlet **set-AzureVMBGInfoExtension** imposta l'estensione BGInfo per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="20bf1-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="20bf1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20bf1-109">EXAMPLES</span></span>

### <span data-ttu-id="20bf1-110">Esempio 1: impostare l'estensione BGInfo per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="20bf1-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="20bf1-111">Questo comando imposta l'estensione BGInfo per la macchina virtuale specificata come archiviato nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="20bf1-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="20bf1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20bf1-112">PARAMETERS</span></span>

### <span data-ttu-id="20bf1-113">-Disable</span><span class="sxs-lookup"><span data-stu-id="20bf1-113">-Disable</span></span>
<span data-ttu-id="20bf1-114">Indica che questo cmdlet disabilita lo stato dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="20bf1-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bf1-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="20bf1-115">-InformationAction</span></span>
<span data-ttu-id="20bf1-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="20bf1-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="20bf1-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="20bf1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20bf1-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="20bf1-118">Continue</span></span>
- <span data-ttu-id="20bf1-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="20bf1-119">Ignore</span></span>
- <span data-ttu-id="20bf1-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="20bf1-120">Inquire</span></span>
- <span data-ttu-id="20bf1-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="20bf1-121">SilentlyContinue</span></span>
- <span data-ttu-id="20bf1-122">Stop</span><span class="sxs-lookup"><span data-stu-id="20bf1-122">Stop</span></span>
- <span data-ttu-id="20bf1-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="20bf1-123">Suspend</span></span>

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

### <span data-ttu-id="20bf1-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="20bf1-124">-InformationVariable</span></span>
<span data-ttu-id="20bf1-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="20bf1-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="20bf1-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="20bf1-126">-Profile</span></span>
<span data-ttu-id="20bf1-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20bf1-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="20bf1-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="20bf1-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20bf1-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="20bf1-129">-ReferenceName</span></span>
<span data-ttu-id="20bf1-130">Specifica il nome di riferimento dell'estensione BGInfo.</span><span class="sxs-lookup"><span data-stu-id="20bf1-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="20bf1-131">Questo parametro è una stringa definita dall'utente che può essere usata per fare riferimento a un'estensione.</span><span class="sxs-lookup"><span data-stu-id="20bf1-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="20bf1-132">Viene specificato quando l'estensione viene aggiunta alla macchina virtuale per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="20bf1-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="20bf1-133">Puoi specificare il nome di riferimento usato in precedenza durante l'aggiornamento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="20bf1-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bf1-134">-Disinstalla</span><span class="sxs-lookup"><span data-stu-id="20bf1-134">-Uninstall</span></span>
<span data-ttu-id="20bf1-135">Indica che questo cmdlet Disinstalla l'estensione BGInfo.</span><span class="sxs-lookup"><span data-stu-id="20bf1-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bf1-136">-Versione</span><span class="sxs-lookup"><span data-stu-id="20bf1-136">-Version</span></span>
<span data-ttu-id="20bf1-137">Specifica la versione dell'estensione BGInfo.</span><span class="sxs-lookup"><span data-stu-id="20bf1-137">Specifies the version of the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20bf1-138">-VM</span><span class="sxs-lookup"><span data-stu-id="20bf1-138">-VM</span></span>
<span data-ttu-id="20bf1-139">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="20bf1-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="20bf1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20bf1-140">CommonParameters</span></span>
<span data-ttu-id="20bf1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20bf1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20bf1-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20bf1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20bf1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20bf1-143">INPUTS</span></span>

## <span data-ttu-id="20bf1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20bf1-144">OUTPUTS</span></span>

## <span data-ttu-id="20bf1-145">Note</span><span class="sxs-lookup"><span data-stu-id="20bf1-145">NOTES</span></span>

## <span data-ttu-id="20bf1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20bf1-146">RELATED LINKS</span></span>

[<span data-ttu-id="20bf1-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="20bf1-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="20bf1-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="20bf1-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


