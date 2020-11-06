---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b9154b239e8d4ae2857cba18d3f7dcf9510a62b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509235"
---
# <span data-ttu-id="7beed-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7beed-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="7beed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7beed-102">SYNOPSIS</span></span>
<span data-ttu-id="7beed-103">Modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7beed-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7beed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7beed-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7beed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7beed-105">DESCRIPTION</span></span>
<span data-ttu-id="7beed-106">Il cmdlet **set-AzureRmDataLakeStoreAccount** modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7beed-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="7beed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7beed-107">EXAMPLES</span></span>

### <span data-ttu-id="7beed-108">Esempio 1: aggiungere un contrassegno a un account</span><span class="sxs-lookup"><span data-stu-id="7beed-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="7beed-109">Questo comando aggiunge il tag specificato all'account di data Lake Store denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="7beed-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="7beed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7beed-110">PARAMETERS</span></span>

### <span data-ttu-id="7beed-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="7beed-111">-AllowAzureIpState</span></span>
<span data-ttu-id="7beed-112">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="7beed-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="7beed-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="7beed-113">-DefaultGroup</span></span>
<span data-ttu-id="7beed-114">Specifica l'ID di un gruppo di directory AzureActive.</span><span class="sxs-lookup"><span data-stu-id="7beed-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="7beed-115">Questo gruppo è il gruppo predefinito per i file e le cartelle creati.</span><span class="sxs-lookup"><span data-stu-id="7beed-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="7beed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7beed-116">-DefaultProfile</span></span>
<span data-ttu-id="7beed-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7beed-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7beed-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="7beed-118">-FirewallState</span></span>
<span data-ttu-id="7beed-119">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="7beed-119">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="7beed-120">-Versione</span><span class="sxs-lookup"><span data-stu-id="7beed-120">-KeyVersion</span></span>
<span data-ttu-id="7beed-121">Se il tipo di crittografia è assegnato dall'utente, l'utente può ruotare la propria versione chiave con questo parametro.</span><span class="sxs-lookup"><span data-stu-id="7beed-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="7beed-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7beed-122">-Name</span></span>
<span data-ttu-id="7beed-123">Specifica il nome di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7beed-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="7beed-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7beed-124">-ResourceGroupName</span></span>
<span data-ttu-id="7beed-125">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da modificare.</span><span class="sxs-lookup"><span data-stu-id="7beed-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="7beed-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="7beed-126">-Tag</span></span>
<span data-ttu-id="7beed-127">Specifica i tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="7beed-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="7beed-128">Puoi usare i tag per identificare un account di data Lake Store da altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="7beed-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7beed-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="7beed-129">-Tier</span></span>
<span data-ttu-id="7beed-130">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="7beed-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="7beed-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="7beed-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="7beed-132">Abilitare o disabilitare facoltativamente i provider di ID attendibili esistenti.</span><span class="sxs-lookup"><span data-stu-id="7beed-132">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="7beed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7beed-133">CommonParameters</span></span>
<span data-ttu-id="7beed-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7beed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7beed-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7beed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7beed-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7beed-136">INPUTS</span></span>

### <span data-ttu-id="7beed-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7beed-137">System.String</span></span>

### <span data-ttu-id="7beed-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7beed-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7beed-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7beed-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7beed-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7beed-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7beed-141">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TierType, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7beed-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7beed-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7beed-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7beed-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7beed-143">OUTPUTS</span></span>

### <span data-ttu-id="7beed-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7beed-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="7beed-145">Note</span><span class="sxs-lookup"><span data-stu-id="7beed-145">NOTES</span></span>

## <span data-ttu-id="7beed-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7beed-146">RELATED LINKS</span></span>

[<span data-ttu-id="7beed-147">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7beed-147">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7beed-148">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7beed-148">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7beed-149">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7beed-149">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7beed-150">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7beed-150">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


