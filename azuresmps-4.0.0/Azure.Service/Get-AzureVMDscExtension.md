---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030000"
---
# <span data-ttu-id="8787f-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8787f-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="8787f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8787f-102">SYNOPSIS</span></span>
<span data-ttu-id="8787f-103">Ottiene le impostazioni dell'estensione DSC in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8787f-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="8787f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8787f-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8787f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8787f-105">DESCRIPTION</span></span>
<span data-ttu-id="8787f-106">Il cmdlet **Get-AzureVMDscExtension** ottiene le impostazioni dell'estensione DSC in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8787f-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="8787f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8787f-107">EXAMPLES</span></span>

### <span data-ttu-id="8787f-108">Esempio 1: ottenere l'impostazione dell'estensione DSC in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="8787f-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="8787f-109">Questo comando consente di ottenere le impostazioni dell'estensione DSC in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8787f-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="8787f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8787f-110">PARAMETERS</span></span>

### <span data-ttu-id="8787f-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8787f-111">-InformationAction</span></span>
<span data-ttu-id="8787f-112">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8787f-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8787f-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8787f-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8787f-114">Continuare</span><span class="sxs-lookup"><span data-stu-id="8787f-114">Continue</span></span>
- <span data-ttu-id="8787f-115">Ignora</span><span class="sxs-lookup"><span data-stu-id="8787f-115">Ignore</span></span>
- <span data-ttu-id="8787f-116">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8787f-116">Inquire</span></span>
- <span data-ttu-id="8787f-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8787f-117">SilentlyContinue</span></span>
- <span data-ttu-id="8787f-118">Stop</span><span class="sxs-lookup"><span data-stu-id="8787f-118">Stop</span></span>
- <span data-ttu-id="8787f-119">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8787f-119">Suspend</span></span>

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

### <span data-ttu-id="8787f-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8787f-120">-InformationVariable</span></span>
<span data-ttu-id="8787f-121">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8787f-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8787f-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="8787f-122">-Profile</span></span>
<span data-ttu-id="8787f-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8787f-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8787f-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8787f-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8787f-125">-VM</span><span class="sxs-lookup"><span data-stu-id="8787f-125">-VM</span></span>
<span data-ttu-id="8787f-126">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="8787f-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8787f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8787f-127">CommonParameters</span></span>
<span data-ttu-id="8787f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8787f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8787f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8787f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8787f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8787f-130">INPUTS</span></span>

## <span data-ttu-id="8787f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8787f-131">OUTPUTS</span></span>

### <span data-ttu-id="8787f-132">Microsoft. WindowsAzure. Commands. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="8787f-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="8787f-133">Note</span><span class="sxs-lookup"><span data-stu-id="8787f-133">NOTES</span></span>

## <span data-ttu-id="8787f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8787f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8787f-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8787f-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="8787f-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8787f-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="8787f-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="8787f-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


