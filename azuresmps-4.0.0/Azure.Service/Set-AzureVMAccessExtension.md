---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023769"
---
# <span data-ttu-id="d3563-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3563-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="d3563-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3563-102">SYNOPSIS</span></span>
<span data-ttu-id="d3563-103">Imposta l'estensione VMAccess per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3563-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="d3563-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3563-104">SYNTAX</span></span>

### <span data-ttu-id="d3563-105">EnableAccessExtension (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3563-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3563-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3563-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3563-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3563-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d3563-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3563-108">DESCRIPTION</span></span>
<span data-ttu-id="d3563-109">Il cmdlet **set-AzureVMAccessExtension** aggiunge l'estensione VMAccess della macchina virtuale a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3563-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="d3563-110">L'estensione VMAccess può essere usata per impostare una password temporanea e questo deve essere immediatamente modificato dopo l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="d3563-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="d3563-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3563-111">EXAMPLES</span></span>

### <span data-ttu-id="d3563-112">Esempio 1: impostare l'estensione VMAccess applicata a una macchina virtuale specificata</span><span class="sxs-lookup"><span data-stu-id="d3563-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="d3563-113">Questo comando imposta l'estensione VMAccess applicata alla macchina virtuale specificata come archiviato nella variabile $VM.</span><span class="sxs-lookup"><span data-stu-id="d3563-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="d3563-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3563-114">PARAMETERS</span></span>

### <span data-ttu-id="d3563-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="d3563-115">-Disable</span></span>
<span data-ttu-id="d3563-116">Indica che questo cmdlet imposta lo stato di estensione su Disable.</span><span class="sxs-lookup"><span data-stu-id="d3563-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3563-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="d3563-117">-ForceUpdate</span></span>
<span data-ttu-id="d3563-118">Indica che questo cmdlet riapplica una configurazione a un'estensione quando la configurazione non è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="d3563-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3563-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d3563-119">-InformationAction</span></span>
<span data-ttu-id="d3563-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d3563-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d3563-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d3563-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d3563-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="d3563-122">Continue</span></span>
- <span data-ttu-id="d3563-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="d3563-123">Ignore</span></span>
- <span data-ttu-id="d3563-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d3563-124">Inquire</span></span>
- <span data-ttu-id="d3563-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d3563-125">SilentlyContinue</span></span>
- <span data-ttu-id="d3563-126">Stop</span><span class="sxs-lookup"><span data-stu-id="d3563-126">Stop</span></span>
- <span data-ttu-id="d3563-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d3563-127">Suspend</span></span>

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

### <span data-ttu-id="d3563-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d3563-128">-InformationVariable</span></span>
<span data-ttu-id="d3563-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d3563-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d3563-130">-Password</span><span class="sxs-lookup"><span data-stu-id="d3563-130">-Password</span></span>
<span data-ttu-id="d3563-131">Specifica la password per reimpostare le credenziali della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3563-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3563-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3563-132">-Profile</span></span>
<span data-ttu-id="d3563-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3563-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3563-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d3563-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3563-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="d3563-135">-ReferenceName</span></span>
<span data-ttu-id="d3563-136">Specifica il nome di riferimento dell'estensione di Access.</span><span class="sxs-lookup"><span data-stu-id="d3563-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="d3563-137">Questa è una stringa definita dall'utente che viene usata per fare riferimento a un'estensione.</span><span class="sxs-lookup"><span data-stu-id="d3563-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="d3563-138">Viene specificato quando l'estensione viene aggiunta alla macchina virtuale per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="d3563-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="d3563-139">Per gli aggiornamenti successivi, devi specificare il nome di riferimento usato in precedenza durante l'aggiornamento dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="d3563-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="d3563-140">Il *riferimento* assegnato a un'estensione viene restituito tramite il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="d3563-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="d3563-141">-Disinstalla</span><span class="sxs-lookup"><span data-stu-id="d3563-141">-Uninstall</span></span>
<span data-ttu-id="d3563-142">Indica se questo cmdlet Disinstalla l'estensione di Access.</span><span class="sxs-lookup"><span data-stu-id="d3563-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3563-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="d3563-143">-UserName</span></span>
<span data-ttu-id="d3563-144">Specifica il nome utente usato da questo cmdlet per reimpostare le credenziali della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3563-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3563-145">-Versione</span><span class="sxs-lookup"><span data-stu-id="d3563-145">-Version</span></span>
<span data-ttu-id="d3563-146">Specifica la versione dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="d3563-146">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3563-147">-VM</span><span class="sxs-lookup"><span data-stu-id="d3563-147">-VM</span></span>
<span data-ttu-id="d3563-148">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="d3563-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d3563-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3563-149">CommonParameters</span></span>
<span data-ttu-id="d3563-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3563-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3563-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3563-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3563-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3563-152">INPUTS</span></span>

## <span data-ttu-id="d3563-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3563-153">OUTPUTS</span></span>

## <span data-ttu-id="d3563-154">Note</span><span class="sxs-lookup"><span data-stu-id="d3563-154">NOTES</span></span>

## <span data-ttu-id="d3563-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3563-155">RELATED LINKS</span></span>

[<span data-ttu-id="d3563-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3563-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="d3563-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="d3563-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


