---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029515"
---
# <span data-ttu-id="64dd9-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="64dd9-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="64dd9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="64dd9-103">Imposta le proprietà di una raccolta RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="64dd9-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="64dd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64dd9-104">SYNTAX</span></span>

### <span data-ttu-id="64dd9-105">DescriptionOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64dd9-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="64dd9-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="64dd9-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="64dd9-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="64dd9-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="64dd9-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="64dd9-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="64dd9-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="64dd9-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64dd9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64dd9-110">DESCRIPTION</span></span>
<span data-ttu-id="64dd9-111">Il cmdlet **set-AzureRemoteAppCollection** imposta le proprietà di una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="64dd9-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="64dd9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64dd9-112">EXAMPLES</span></span>

## <span data-ttu-id="64dd9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64dd9-113">PARAMETERS</span></span>

### <span data-ttu-id="64dd9-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="64dd9-114">-AclLevel</span></span>
<span data-ttu-id="64dd9-115">Specifica il livello dell'elenco di controllo di accesso (ACL) per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="64dd9-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="64dd9-116">I valori accettabili per questo parametro sono: Collection e Application.</span><span class="sxs-lookup"><span data-stu-id="64dd9-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dd9-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="64dd9-117">-CollectionName</span></span>
<span data-ttu-id="64dd9-118">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="64dd9-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dd9-119">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="64dd9-119">-Credential</span></span>
<span data-ttu-id="64dd9-120">Specifica le credenziali di un account del servizio con l'autorizzazione per l'accesso ai server RemoteApp di Azure al dominio.</span><span class="sxs-lookup"><span data-stu-id="64dd9-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="64dd9-121">Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="64dd9-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dd9-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="64dd9-122">-CustomRdpProperty</span></span>
<span data-ttu-id="64dd9-123">Specifica le proprietà Remote Desktop Protocol (RDP) personalizzate che possono essere usate per configurare il reindirizzamento delle unità e altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="64dd9-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="64dd9-124">Per informazioni dettagliate, vedere [Impostazioni RDP per Servizi Desktop remoto in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="64dd9-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dd9-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="64dd9-125">-Description</span></span>
<span data-ttu-id="64dd9-126">Specifica una breve descrizione per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="64dd9-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dd9-127">-Piano</span><span class="sxs-lookup"><span data-stu-id="64dd9-127">-Plan</span></span>
<span data-ttu-id="64dd9-128">Specifica il piano per la raccolta RemoteApp di Azure, che definisce i limiti di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="64dd9-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="64dd9-129">Usare **Get-AzureRemoteAppPlan** per visualizzare i piani disponibili.</span><span class="sxs-lookup"><span data-stu-id="64dd9-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64dd9-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="64dd9-130">-Profile</span></span>
<span data-ttu-id="64dd9-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64dd9-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64dd9-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="64dd9-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64dd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dd9-133">CommonParameters</span></span>
<span data-ttu-id="64dd9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dd9-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64dd9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dd9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64dd9-136">INPUTS</span></span>

## <span data-ttu-id="64dd9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64dd9-137">OUTPUTS</span></span>

## <span data-ttu-id="64dd9-138">Note</span><span class="sxs-lookup"><span data-stu-id="64dd9-138">NOTES</span></span>

## <span data-ttu-id="64dd9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64dd9-139">RELATED LINKS</span></span>

[<span data-ttu-id="64dd9-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="64dd9-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="64dd9-141">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="64dd9-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="64dd9-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="64dd9-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


