---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023954"
---
# <span data-ttu-id="8d382-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8d382-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="8d382-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d382-102">SYNOPSIS</span></span>
<span data-ttu-id="8d382-103">Crea una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8d382-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d382-104">SYNTAX</span></span>

### <span data-ttu-id="8d382-105">AllParameterSets (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8d382-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8d382-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="8d382-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8d382-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d382-107">DESCRIPTION</span></span>
<span data-ttu-id="8d382-108">Il cmdlet **New-AzureRemoteAppCollection** crea una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="8d382-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d382-109">EXAMPLES</span></span>

### <span data-ttu-id="8d382-110">Esempio 1: creare una raccolta</span><span class="sxs-lookup"><span data-stu-id="8d382-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="8d382-111">Questo comando crea una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="8d382-112">Esempio 2: creare una raccolta usando le credenziali</span><span class="sxs-lookup"><span data-stu-id="8d382-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="8d382-113">Questo comando crea una raccolta RemoteApp di Azure utilizzando una credenziale del cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="8d382-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="8d382-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d382-114">PARAMETERS</span></span>

### <span data-ttu-id="8d382-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="8d382-115">-CollectionName</span></span>
<span data-ttu-id="8d382-116">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-116">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="8d382-117">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="8d382-117">-Credential</span></span>
<span data-ttu-id="8d382-118">Specifica le credenziali di un account del servizio con l'autorizzazione per l'accesso ai server RemoteApp di Azure al dominio.</span><span class="sxs-lookup"><span data-stu-id="8d382-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="8d382-119">Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="8d382-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="8d382-120">-CustomRdpProperty</span></span>
<span data-ttu-id="8d382-121">Specifica le proprietà di desktop remoto personalizzate (RDP) che possono essere usate per configurare il reindirizzamento delle unità e altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="8d382-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="8d382-122">Per informazioni dettagliate, vedere [Impostazioni RDP per Servizi Desktop remoto in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="8d382-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

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

### <span data-ttu-id="8d382-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d382-123">-Description</span></span>
<span data-ttu-id="8d382-124">Specifica una breve descrizione per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8d382-124">Specifies a short description for the object.</span></span>

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

### <span data-ttu-id="8d382-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="8d382-125">-DnsServers</span></span>
<span data-ttu-id="8d382-126">Specifica un elenco delimitato da virgole di indirizzi IPv4 dei server DNS.</span><span class="sxs-lookup"><span data-stu-id="8d382-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="8d382-127">-Domain</span></span>
<span data-ttu-id="8d382-128">Specifica il nome del dominio dei servizi di dominio Active Directory a cui partecipare ai server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="8d382-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="8d382-129">-ImageName</span></span>
<span data-ttu-id="8d382-130">Specifica il nome dell'immagine del modello RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8d382-131">-Location</span></span>
<span data-ttu-id="8d382-132">Specifica l'area di Azure della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8d382-132">Specifies the Azure region of the collection.</span></span>

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

### <span data-ttu-id="8d382-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="8d382-133">-OrganizationalUnit</span></span>
<span data-ttu-id="8d382-134">Specifica il nome dell'unità organizzativa a cui partecipare ai server Host sessione Desktop remoto, ad esempio OU = MyOu, DC = dominio, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="8d382-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="8d382-135">Gli attributi come OU e DC devono essere in maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="8d382-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="8d382-136">L'unità organizzativa non può essere modificata dopo la creazione della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8d382-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-137">-Piano</span><span class="sxs-lookup"><span data-stu-id="8d382-137">-Plan</span></span>
<span data-ttu-id="8d382-138">Specifica il piano per la raccolta RemoteApp di Azure, che può definire i limiti di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="8d382-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="8d382-139">Usare **Get-AzureRemoteAppPlan** per visualizzare i piani disponibili.</span><span class="sxs-lookup"><span data-stu-id="8d382-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="8d382-140">-Profile</span></span>
<span data-ttu-id="8d382-141">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d382-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8d382-142">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8d382-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8d382-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8d382-143">-ResourceType</span></span>
<span data-ttu-id="8d382-144">Specifica il tipo di risorsa della raccolta.</span><span class="sxs-lookup"><span data-stu-id="8d382-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="8d382-145">I valori accettabili per questo parametro sono: app o desktop.</span><span class="sxs-lookup"><span data-stu-id="8d382-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="8d382-146">-SubnetName</span></span>
<span data-ttu-id="8d382-147">Specifica il nome della subnet nella rete virtuale da usare per creare la raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d382-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="8d382-148">-VNetName</span></span>
<span data-ttu-id="8d382-149">Specifica il nome di una rete virtuale di Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8d382-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d382-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d382-150">CommonParameters</span></span>
<span data-ttu-id="8d382-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d382-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d382-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d382-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d382-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d382-153">INPUTS</span></span>

## <span data-ttu-id="8d382-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d382-154">OUTPUTS</span></span>

## <span data-ttu-id="8d382-155">Note</span><span class="sxs-lookup"><span data-stu-id="8d382-155">NOTES</span></span>

## <span data-ttu-id="8d382-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d382-156">RELATED LINKS</span></span>

[<span data-ttu-id="8d382-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8d382-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="8d382-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="8d382-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="8d382-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8d382-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="8d382-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8d382-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="8d382-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="8d382-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


