---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: b0e52f6d163579e1d481f841d3a58e8b15c6658b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012429"
---
# <span data-ttu-id="3952c-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="3952c-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="3952c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3952c-102">SYNOPSIS</span></span>
<span data-ttu-id="3952c-103">API per registrare un nuovo computer e quindi creare una risorsa tracciata in ARM</span><span class="sxs-lookup"><span data-stu-id="3952c-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="3952c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3952c-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="3952c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3952c-105">DESCRIPTION</span></span>
<span data-ttu-id="3952c-106">API per registrare un nuovo computer e quindi creare una risorsa tracciata in ARM</span><span class="sxs-lookup"><span data-stu-id="3952c-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="3952c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3952c-107">EXAMPLES</span></span>

### <span data-ttu-id="3952c-108">Esempio 1: eseguire l'onboards del computer in uso come computer connesso</span><span class="sxs-lookup"><span data-stu-id="3952c-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="3952c-109">Onboards il computer su cui ti stai collegando come computer connesso.</span><span class="sxs-lookup"><span data-stu-id="3952c-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="3952c-110">Esempio 2: consente di aggiungere un computer remoto come dispositivo connesso</span><span class="sxs-lookup"><span data-stu-id="3952c-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="3952c-111">Consente di eseguire l'onboardmento di un computer remoto come dispositivo connesso tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3952c-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="3952c-112">Nota: al momento è supportato solo Windows come destinazione.</span><span class="sxs-lookup"><span data-stu-id="3952c-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="3952c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3952c-113">PARAMETERS</span></span>

### <span data-ttu-id="3952c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3952c-114">-DefaultProfile</span></span>
<span data-ttu-id="3952c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3952c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3952c-116">-Location</span></span>
<span data-ttu-id="3952c-117">Posizione della macchina connessa creata.</span><span class="sxs-lookup"><span data-stu-id="3952c-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3952c-118">-Name</span></span>
<span data-ttu-id="3952c-119">Nome che verrà usato per il computer.</span><span class="sxs-lookup"><span data-stu-id="3952c-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="3952c-120">Il nome host viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3952c-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="3952c-121">-Proxy</span></span>
<span data-ttu-id="3952c-122">URI da usare per il server proxy</span><span class="sxs-lookup"><span data-stu-id="3952c-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="3952c-123">-PSSession</span></span>
<span data-ttu-id="3952c-124">Se specificato, il comando che esegue l'onboarder di computer in Azure viene eseguito in ogni PSSession.</span><span class="sxs-lookup"><span data-stu-id="3952c-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="3952c-125">NOTA: per il momento questa operazione funziona solo in Windows.</span><span class="sxs-lookup"><span data-stu-id="3952c-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3952c-126">-ResourceGroupName</span></span>
<span data-ttu-id="3952c-127">Nome del gruppo di risorse a cui si vuole aggiungere il computer.</span><span class="sxs-lookup"><span data-stu-id="3952c-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3952c-128">-SubscriptionId</span></span>
<span data-ttu-id="3952c-129">ID dell'abbonamento a cui si vuole aggiungere il computer.</span><span class="sxs-lookup"><span data-stu-id="3952c-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="3952c-130">-Tag</span></span>
<span data-ttu-id="3952c-131">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="3952c-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3952c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3952c-132">CommonParameters</span></span>
<span data-ttu-id="3952c-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3952c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3952c-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3952c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3952c-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="3952c-135">INPUTS</span></span>

## <span data-ttu-id="3952c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3952c-136">OUTPUTS</span></span>

## <span data-ttu-id="3952c-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="3952c-137">NOTES</span></span>

<span data-ttu-id="3952c-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3952c-138">ALIASES</span></span>

## <span data-ttu-id="3952c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3952c-139">RELATED LINKS</span></span>

