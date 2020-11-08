---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023807"
---
# <span data-ttu-id="e6de9-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="e6de9-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="e6de9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6de9-102">SYNOPSIS</span></span>
<span data-ttu-id="e6de9-103">Imposta l'estensione marionetta per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6de9-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="e6de9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6de9-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6de9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6de9-105">DESCRIPTION</span></span>
<span data-ttu-id="e6de9-106">Il cmdlet **set-AzureVMPuppetExtension** imposta l'estensione marionetta per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e6de9-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="e6de9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6de9-107">EXAMPLES</span></span>

### <span data-ttu-id="e6de9-108">Esempio 1: impostare l'estensione marionetta per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="e6de9-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="e6de9-109">Questo esempio imposta l'estensione marionetta per la macchina virtuale specificata come archiviato nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="e6de9-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="e6de9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6de9-110">PARAMETERS</span></span>

### <span data-ttu-id="e6de9-111">-Disable</span><span class="sxs-lookup"><span data-stu-id="e6de9-111">-Disable</span></span>
<span data-ttu-id="e6de9-112">Indica che questo cmdlet disabilita lo stato dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e6de9-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6de9-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e6de9-113">-InformationAction</span></span>
<span data-ttu-id="e6de9-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="e6de9-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6de9-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6de9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6de9-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="e6de9-116">Continue</span></span>
- <span data-ttu-id="e6de9-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="e6de9-117">Ignore</span></span>
- <span data-ttu-id="e6de9-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="e6de9-118">Inquire</span></span>
- <span data-ttu-id="e6de9-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6de9-119">SilentlyContinue</span></span>
- <span data-ttu-id="e6de9-120">Stop</span><span class="sxs-lookup"><span data-stu-id="e6de9-120">Stop</span></span>
- <span data-ttu-id="e6de9-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="e6de9-121">Suspend</span></span>

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

### <span data-ttu-id="e6de9-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6de9-122">-InformationVariable</span></span>
<span data-ttu-id="e6de9-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="e6de9-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e6de9-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6de9-124">-Profile</span></span>
<span data-ttu-id="e6de9-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6de9-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6de9-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e6de9-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6de9-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="e6de9-127">-PuppetMasterServer</span></span>
<span data-ttu-id="e6de9-128">Specifica il nome di dominio completo (FQDN) del server master Puppet.</span><span class="sxs-lookup"><span data-stu-id="e6de9-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6de9-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="e6de9-129">-ReferenceName</span></span>
<span data-ttu-id="e6de9-130">Specifica il nome di riferimento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e6de9-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="e6de9-131">Questa è una stringa definita dall'utente che viene usata per fare riferimento a un'estensione.</span><span class="sxs-lookup"><span data-stu-id="e6de9-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="e6de9-132">Viene specificato quando l'estensione viene aggiunta alla macchina virtuale per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="e6de9-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="e6de9-133">Per gli aggiornamenti successivi, è necessario specificare il nome di riferimento usato in precedenza quando si aggiorna l'estensione.</span><span class="sxs-lookup"><span data-stu-id="e6de9-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="e6de9-134">Il riferimento assegnato a un'estensione viene restituito tramite il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="e6de9-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6de9-135">-Versione</span><span class="sxs-lookup"><span data-stu-id="e6de9-135">-Version</span></span>
<span data-ttu-id="e6de9-136">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e6de9-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="e6de9-137">-VM</span><span class="sxs-lookup"><span data-stu-id="e6de9-137">-VM</span></span>
<span data-ttu-id="e6de9-138">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="e6de9-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="e6de9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6de9-139">CommonParameters</span></span>
<span data-ttu-id="e6de9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6de9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6de9-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6de9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6de9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6de9-142">INPUTS</span></span>

## <span data-ttu-id="e6de9-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6de9-143">OUTPUTS</span></span>

## <span data-ttu-id="e6de9-144">Note</span><span class="sxs-lookup"><span data-stu-id="e6de9-144">NOTES</span></span>

## <span data-ttu-id="e6de9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6de9-145">RELATED LINKS</span></span>

[<span data-ttu-id="e6de9-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6de9-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


