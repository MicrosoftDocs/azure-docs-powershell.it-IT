---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BE661AC7-BA39-4D6A-8083-16CE9327DC08
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4c84155484435a9601af005393593040c9cfe4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029810"
---
# <span data-ttu-id="654bf-101">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="654bf-101">Get-AzureIPForwarding</span></span>

## <span data-ttu-id="654bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="654bf-102">SYNOPSIS</span></span>
<span data-ttu-id="654bf-103">Ottiene lo stato di inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="654bf-103">Gets the status of IP forwarding.</span></span>

## <span data-ttu-id="654bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="654bf-104">SYNTAX</span></span>

### <span data-ttu-id="654bf-105">IaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="654bf-105">IaaSIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="654bf-106">SlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="654bf-106">SlotIPForwardingParamSet</span></span>
```
Get-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="654bf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="654bf-107">DESCRIPTION</span></span>
<span data-ttu-id="654bf-108">Il cmdlet **Get-AzureIPForwarding** ottiene lo stato di inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="654bf-108">The **Get-AzureIPForwarding** cmdlet gets the status of IP forwarding.</span></span>

## <span data-ttu-id="654bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="654bf-109">EXAMPLES</span></span>

### <span data-ttu-id="654bf-110">Esempio 1: ottenere lo stato di inoltro IP per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="654bf-110">Example 1: Get IP forwarding status for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureIPForwarding
Disabled
```

<span data-ttu-id="654bf-111">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="654bf-111">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="654bf-112">Il cmdlet corrente ottiene lo stato di inoltro IP per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="654bf-112">The current cmdlet gets the status of IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="654bf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="654bf-113">PARAMETERS</span></span>

### <span data-ttu-id="654bf-114">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="654bf-114">-NetworkInterfaceName</span></span>
<span data-ttu-id="654bf-115">Specifica il nome della scheda di rete per cui questo cmdlet ottiene lo stato di inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="654bf-115">Specifies the name of the network adapter for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654bf-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="654bf-116">-Profile</span></span>
<span data-ttu-id="654bf-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="654bf-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="654bf-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="654bf-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="654bf-119">-RoleName</span><span class="sxs-lookup"><span data-stu-id="654bf-119">-RoleName</span></span>
<span data-ttu-id="654bf-120">Specifica il nome di un ruolo PaaS per il quale questo cmdlet ottiene lo stato di inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="654bf-120">Specifies the name of a PaaS role for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654bf-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="654bf-121">-ServiceName</span></span>
<span data-ttu-id="654bf-122">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="654bf-122">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="654bf-123">Il ruolo PaaS appartiene al servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="654bf-123">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="654bf-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="654bf-124">-Slot</span></span>
<span data-ttu-id="654bf-125">Specifica uno slot PaaS.</span><span class="sxs-lookup"><span data-stu-id="654bf-125">Specifies a PaaS slot.</span></span>
<span data-ttu-id="654bf-126">Il ruolo PaaS per cui questo cmdlet ottiene lo stato di inoltro include lo slot specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="654bf-126">The PaaS role for which this cmdlet gets forwarding status has the slot that this parameter specifies.</span></span>
<span data-ttu-id="654bf-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="654bf-127">Valid values are:</span></span> 

- <span data-ttu-id="654bf-128">Produzione</span><span class="sxs-lookup"><span data-stu-id="654bf-128">Production</span></span>
- <span data-ttu-id="654bf-129">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="654bf-129">Staging</span></span> 

<span data-ttu-id="654bf-130">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="654bf-130">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: SlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="654bf-131">-VM</span><span class="sxs-lookup"><span data-stu-id="654bf-131">-VM</span></span>
<span data-ttu-id="654bf-132">Specifica l'oggetto macchina virtuale per cui questo cmdlet ottiene lo stato di inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="654bf-132">Specifies the virtual machine object for which this cmdlet gets IP forwarding status.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: IaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="654bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="654bf-133">CommonParameters</span></span>
<span data-ttu-id="654bf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="654bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="654bf-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="654bf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="654bf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="654bf-136">INPUTS</span></span>

## <span data-ttu-id="654bf-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="654bf-137">OUTPUTS</span></span>

### <span data-ttu-id="654bf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="654bf-138">System.String</span></span>

## <span data-ttu-id="654bf-139">Note</span><span class="sxs-lookup"><span data-stu-id="654bf-139">NOTES</span></span>

## <span data-ttu-id="654bf-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="654bf-140">RELATED LINKS</span></span>

[<span data-ttu-id="654bf-141">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="654bf-141">Set-AzureIPForwarding</span></span>](./Set-AzureIPForwarding.md)


