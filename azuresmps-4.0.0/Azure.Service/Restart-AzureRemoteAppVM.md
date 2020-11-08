---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029546"
---
# <span data-ttu-id="79b23-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="79b23-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="79b23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79b23-102">SYNOPSIS</span></span>
<span data-ttu-id="79b23-103">Riavvia una macchina virtuale in una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="79b23-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="79b23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79b23-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b23-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79b23-105">DESCRIPTION</span></span>
<span data-ttu-id="79b23-106">Il cmdlet **Restart-AzureRemoteAppVM riavvia** una macchina virtuale in una raccolta RemoteApp di Azure in cui l'utente specificato è connesso.</span><span class="sxs-lookup"><span data-stu-id="79b23-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="79b23-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79b23-107">EXAMPLES</span></span>

### <span data-ttu-id="79b23-108">Esempio 1: riavviare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="79b23-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="79b23-109">Questo comando Riavvia una macchina virtuale in una raccolta RemoteApp di Azure denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="79b23-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="79b23-110">L'utente PattiFuller@contoso.com è connesso alla raccolta che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="79b23-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="79b23-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79b23-111">PARAMETERS</span></span>

### <span data-ttu-id="79b23-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="79b23-112">-CollectionName</span></span>
<span data-ttu-id="79b23-113">Specifica il nome di una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="79b23-113">Specifies the name of an Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b23-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="79b23-114">-LogoffMessage</span></span>
<span data-ttu-id="79b23-115">Specifica un messaggio di avviso visualizzato agli utenti connessi alla macchina virtuale prima che il cmdlet li registri.</span><span class="sxs-lookup"><span data-stu-id="79b23-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79b23-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="79b23-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="79b23-117">Specifica il periodo di attesa di questo cmdlet prima che gli utenti registrino la disattivazione.</span><span class="sxs-lookup"><span data-stu-id="79b23-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="79b23-118">Il valore predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="79b23-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79b23-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="79b23-119">-Profile</span></span>
<span data-ttu-id="79b23-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b23-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79b23-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="79b23-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79b23-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="79b23-122">-UserUpn</span></span>
<span data-ttu-id="79b23-123">Specifica il nome dell'entità utente (UPN) dell'utente per cui questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="79b23-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="79b23-124">Per ottenere macchine virtuali nella raccolta e UPN connesse, usare il cmdlet **Get-AzureRemoteAppVM** .</span><span class="sxs-lookup"><span data-stu-id="79b23-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79b23-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79b23-125">-Confirm</span></span>
<span data-ttu-id="79b23-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b23-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b23-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b23-127">-WhatIf</span></span>
<span data-ttu-id="79b23-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79b23-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b23-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79b23-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b23-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b23-130">CommonParameters</span></span>
<span data-ttu-id="79b23-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b23-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b23-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b23-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b23-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79b23-133">INPUTS</span></span>

## <span data-ttu-id="79b23-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79b23-134">OUTPUTS</span></span>

## <span data-ttu-id="79b23-135">Note</span><span class="sxs-lookup"><span data-stu-id="79b23-135">NOTES</span></span>

## <span data-ttu-id="79b23-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79b23-136">RELATED LINKS</span></span>

[<span data-ttu-id="79b23-137">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="79b23-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


