---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033238"
---
# <span data-ttu-id="c1eb9-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="c1eb9-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="c1eb9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c1eb9-103">API per registrare un nuovo computer e quindi creare una risorsa rilevata in ARM</span><span class="sxs-lookup"><span data-stu-id="c1eb9-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c1eb9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1eb9-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="c1eb9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="c1eb9-106">API per registrare un nuovo computer e quindi creare una risorsa rilevata in ARM</span><span class="sxs-lookup"><span data-stu-id="c1eb9-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="c1eb9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="c1eb9-108">Esempio 1: onboards il computer in cui ci si trova come computer connesso</span><span class="sxs-lookup"><span data-stu-id="c1eb9-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="c1eb9-109">A bordo della macchina in cui ci si trova come computer connesso.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="c1eb9-110">Esempio 2: bordo di un computer remoto come dispositivo connesso</span><span class="sxs-lookup"><span data-stu-id="c1eb9-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="c1eb9-111">Onboards un computer remoto come dispositivo connesso tramite la comunicazione remota di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="c1eb9-112">Nota: in questo momento sono supportate solo le finestre come destinazione.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="c1eb9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1eb9-113">PARAMETERS</span></span>

### <span data-ttu-id="c1eb9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1eb9-114">-DefaultProfile</span></span>
<span data-ttu-id="c1eb9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1eb9-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c1eb9-116">-Location</span></span>
<span data-ttu-id="c1eb9-117">La posizione per il ConnectedMachine creato.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="c1eb9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1eb9-118">-Name</span></span>
<span data-ttu-id="c1eb9-119">Nome che verrà usato per questo computer.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="c1eb9-120">Il nome host viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="c1eb9-121">-Proxy</span><span class="sxs-lookup"><span data-stu-id="c1eb9-121">-Proxy</span></span>
<span data-ttu-id="c1eb9-122">URI per il server proxy da usare</span><span class="sxs-lookup"><span data-stu-id="c1eb9-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="c1eb9-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="c1eb9-123">-PSSession</span></span>
<span data-ttu-id="c1eb9-124">Se specificato, il comando che viene eseguito da computer a Azure verrà eseguita all'interno di ogni sessione PSSession.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="c1eb9-125">Nota: questo funziona solo su Windows per ora.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="c1eb9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1eb9-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1eb9-127">Nome del gruppo di risorse a cui si vuole aggiungere il computer.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="c1eb9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1eb9-128">-SubscriptionId</span></span>
<span data-ttu-id="c1eb9-129">ID dell'abbonamento a cui si vuole aggiungere il computer.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="c1eb9-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1eb9-130">-Tag</span></span>
<span data-ttu-id="c1eb9-131">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-131">Resource tags.</span></span>

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

### <span data-ttu-id="c1eb9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1eb9-132">CommonParameters</span></span>
<span data-ttu-id="c1eb9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1eb9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1eb9-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1eb9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1eb9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1eb9-135">INPUTS</span></span>

## <span data-ttu-id="c1eb9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1eb9-136">OUTPUTS</span></span>

## <span data-ttu-id="c1eb9-137">Note</span><span class="sxs-lookup"><span data-stu-id="c1eb9-137">NOTES</span></span>

<span data-ttu-id="c1eb9-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c1eb9-138">ALIASES</span></span>

## <span data-ttu-id="c1eb9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1eb9-139">RELATED LINKS</span></span>

