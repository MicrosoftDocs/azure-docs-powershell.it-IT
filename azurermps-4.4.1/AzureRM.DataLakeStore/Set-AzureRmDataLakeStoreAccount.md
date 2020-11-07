---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f9ebe1a541baf46e831dbe95b54b2881a03e7454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686844"
---
# <span data-ttu-id="c1ea1-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1ea1-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="c1ea1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ea1-103">Modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1ea1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1ea1-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tags] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1ea1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="c1ea1-106">Il cmdlet **set-AzureRmDataLakeStoreAccount** modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="c1ea1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="c1ea1-108">Esempio 1: aggiungere un contrassegno a un account</span><span class="sxs-lookup"><span data-stu-id="c1ea1-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="c1ea1-109">Questo comando aggiunge il tag specificato all'account di data Lake Store denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="c1ea1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1ea1-110">PARAMETERS</span></span>

### <span data-ttu-id="c1ea1-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="c1ea1-111">-AllowAzureIpState</span></span>
<span data-ttu-id="c1ea1-112">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="c1ea1-113">-DefaultGroup</span></span>
<span data-ttu-id="c1ea1-114">Specifica l'ID di un gruppo di directory AzureActive.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="c1ea1-115">Questo gruppo è il gruppo predefinito per i file e le cartelle creati.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-116">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="c1ea1-116">-FirewallState</span></span>
<span data-ttu-id="c1ea1-117">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-117">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-118">-Versione</span><span class="sxs-lookup"><span data-stu-id="c1ea1-118">-KeyVersion</span></span>
<span data-ttu-id="c1ea1-119">Se il tipo di crittografia è assegnato dall'utente, l'utente può ruotare la propria versione chiave con questo parametro.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-119">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1ea1-120">-Name</span></span>
<span data-ttu-id="c1ea1-121">Specifica il nome di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-121">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ea1-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1ea1-123">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da modificare.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-123">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="c1ea1-124">-Tags</span></span>
<span data-ttu-id="c1ea1-125">Specifica i tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-125">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="c1ea1-126">Puoi usare i tag per identificare un account di data Lake Store da altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-126">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="c1ea1-127">-Tier</span></span>
<span data-ttu-id="c1ea1-128">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-128">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-129">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="c1ea1-129">-TrustedIdProviderState</span></span>
<span data-ttu-id="c1ea1-130">Abilitare o disabilitare facoltativamente i provider di ID attendibili esistenti.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-130">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1ea1-131">-DefaultProfile</span></span>
<span data-ttu-id="c1ea1-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1ea1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ea1-133">CommonParameters</span></span>
<span data-ttu-id="c1ea1-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ea1-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1ea1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ea1-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1ea1-136">INPUTS</span></span>

## <span data-ttu-id="c1ea1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1ea1-137">OUTPUTS</span></span>

### <span data-ttu-id="c1ea1-138">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1ea1-138">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="c1ea1-139">Dettagli dell'account aggiornato.</span><span class="sxs-lookup"><span data-stu-id="c1ea1-139">The updated account details.</span></span>

## <span data-ttu-id="c1ea1-140">Note</span><span class="sxs-lookup"><span data-stu-id="c1ea1-140">NOTES</span></span>

## <span data-ttu-id="c1ea1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1ea1-141">RELATED LINKS</span></span>

[<span data-ttu-id="c1ea1-142">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1ea1-142">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c1ea1-143">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1ea1-143">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c1ea1-144">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1ea1-144">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c1ea1-145">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1ea1-145">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


