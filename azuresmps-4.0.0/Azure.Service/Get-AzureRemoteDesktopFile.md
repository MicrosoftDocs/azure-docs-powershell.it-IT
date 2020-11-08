---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023578"
---
# <span data-ttu-id="5de57-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="5de57-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="5de57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5de57-102">SYNOPSIS</span></span>
<span data-ttu-id="5de57-103">Ottiene un file RDP per una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5de57-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="5de57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5de57-104">SYNTAX</span></span>

### <span data-ttu-id="5de57-105">Download (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5de57-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5de57-106">Avvio</span><span class="sxs-lookup"><span data-stu-id="5de57-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5de57-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5de57-107">DESCRIPTION</span></span>
<span data-ttu-id="5de57-108">Il cmdlet **Get-AzureRemoteDesktopFile** consente di scaricare e salvare un file di connessione Desktop remoto (RDP) per una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="5de57-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="5de57-109">Il cmdlet può avviare una connessione Desktop remoto alla macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="5de57-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="5de57-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5de57-110">EXAMPLES</span></span>

### <span data-ttu-id="5de57-111">Esempio 1: ottenere un file RDP</span><span class="sxs-lookup"><span data-stu-id="5de57-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="5de57-112">Questo comando ottiene un file RDP per la macchina virtuale VirtualMachine07 denominata VirtualMachine07 che viene eseguito nel servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="5de57-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="5de57-113">Il comando Archivia il file come C:\temp\VirtualMachine07.rdp.</span><span class="sxs-lookup"><span data-stu-id="5de57-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="5de57-114">Esempio 2: avviare una sessione remota</span><span class="sxs-lookup"><span data-stu-id="5de57-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="5de57-115">Questo comando ottiene un file RDP per la macchina virtuale VirtualMachine07 denominata VirtualMachine07 che viene eseguito nel servizio denominato ContosoService.</span><span class="sxs-lookup"><span data-stu-id="5de57-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="5de57-116">Il comando avvia una sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="5de57-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="5de57-117">Il comando Elimina il file RDP quando la connessione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="5de57-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="5de57-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5de57-118">PARAMETERS</span></span>

### <span data-ttu-id="5de57-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5de57-119">-InformationAction</span></span>
<span data-ttu-id="5de57-120">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="5de57-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5de57-121">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5de57-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5de57-122">Continuare</span><span class="sxs-lookup"><span data-stu-id="5de57-122">Continue</span></span>
- <span data-ttu-id="5de57-123">Ignora</span><span class="sxs-lookup"><span data-stu-id="5de57-123">Ignore</span></span>
- <span data-ttu-id="5de57-124">Informarsi</span><span class="sxs-lookup"><span data-stu-id="5de57-124">Inquire</span></span>
- <span data-ttu-id="5de57-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5de57-125">SilentlyContinue</span></span>
- <span data-ttu-id="5de57-126">Stop</span><span class="sxs-lookup"><span data-stu-id="5de57-126">Stop</span></span>
- <span data-ttu-id="5de57-127">Sospensione</span><span class="sxs-lookup"><span data-stu-id="5de57-127">Suspend</span></span>

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

### <span data-ttu-id="5de57-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5de57-128">-InformationVariable</span></span>
<span data-ttu-id="5de57-129">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="5de57-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5de57-130">-Avvio</span><span class="sxs-lookup"><span data-stu-id="5de57-130">-Launch</span></span>
<span data-ttu-id="5de57-131">Indica che il cmdlet avvia una sessione Desktop remoto nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5de57-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de57-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="5de57-132">-LocalPath</span></span>
<span data-ttu-id="5de57-133">Specifica il percorso completo del file RDP scaricato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="5de57-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5de57-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="5de57-134">-Name</span></span>
<span data-ttu-id="5de57-135">Specifica la macchina virtuale per cui questo cmdlet Scarica un file RDP.</span><span class="sxs-lookup"><span data-stu-id="5de57-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5de57-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="5de57-136">-Profile</span></span>
<span data-ttu-id="5de57-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5de57-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5de57-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5de57-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5de57-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5de57-139">-ServiceName</span></span>
<span data-ttu-id="5de57-140">Specifica il nome del servizio Azure a cui appartiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5de57-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5de57-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de57-141">CommonParameters</span></span>
<span data-ttu-id="5de57-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de57-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de57-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de57-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de57-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5de57-144">INPUTS</span></span>

## <span data-ttu-id="5de57-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5de57-145">OUTPUTS</span></span>

## <span data-ttu-id="5de57-146">Note</span><span class="sxs-lookup"><span data-stu-id="5de57-146">NOTES</span></span>

## <span data-ttu-id="5de57-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5de57-147">RELATED LINKS</span></span>

