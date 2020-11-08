---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029907"
---
# <span data-ttu-id="13220-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="13220-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="13220-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13220-102">SYNOPSIS</span></span>
<span data-ttu-id="13220-103">Rimuove la configurazione del disco del sistema operativo dall'oggetto DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="13220-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="13220-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13220-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="13220-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13220-105">DESCRIPTION</span></span>
<span data-ttu-id="13220-106">Il cmdlet **Remove-AzureVMImageOSDiskConfig** rimuove la configurazione del disco del sistema operativo dall'oggetto DiskConfigSet.</span><span class="sxs-lookup"><span data-stu-id="13220-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="13220-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13220-107">EXAMPLES</span></span>

### <span data-ttu-id="13220-108">Esempio 1: rimuovere la configurazione del disco del sistema operativo da un DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="13220-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="13220-109">Questo comando rimuove la configurazione del disco del sistema operativo dall'oggetto DiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="13220-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="13220-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13220-110">PARAMETERS</span></span>

### <span data-ttu-id="13220-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="13220-111">-DiskConfig</span></span>
<span data-ttu-id="13220-112">Specifica l'oggetto di configurazione del disco che incapsula il disco del sistema operativo e gli oggetti del disco di dati.</span><span class="sxs-lookup"><span data-stu-id="13220-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13220-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="13220-113">-InformationAction</span></span>
<span data-ttu-id="13220-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="13220-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13220-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="13220-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13220-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="13220-116">Continue</span></span>
- <span data-ttu-id="13220-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="13220-117">Ignore</span></span>
- <span data-ttu-id="13220-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="13220-118">Inquire</span></span>
- <span data-ttu-id="13220-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13220-119">SilentlyContinue</span></span>
- <span data-ttu-id="13220-120">Stop</span><span class="sxs-lookup"><span data-stu-id="13220-120">Stop</span></span>
- <span data-ttu-id="13220-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="13220-121">Suspend</span></span>

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

### <span data-ttu-id="13220-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13220-122">-InformationVariable</span></span>
<span data-ttu-id="13220-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="13220-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13220-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13220-124">CommonParameters</span></span>
<span data-ttu-id="13220-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13220-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13220-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13220-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13220-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13220-127">INPUTS</span></span>

## <span data-ttu-id="13220-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13220-128">OUTPUTS</span></span>

### <span data-ttu-id="13220-129">Microsoft. WindowsAzure. Commands. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="13220-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="13220-130">Note</span><span class="sxs-lookup"><span data-stu-id="13220-130">NOTES</span></span>

## <span data-ttu-id="13220-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13220-131">RELATED LINKS</span></span>

[<span data-ttu-id="13220-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="13220-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


