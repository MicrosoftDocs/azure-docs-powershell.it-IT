---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511200"
---
# <span data-ttu-id="afd5b-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="afd5b-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="afd5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="afd5b-103">Modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="afd5b-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afd5b-104">SYNTAX</span></span>

### <span data-ttu-id="afd5b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="afd5b-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd5b-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="afd5b-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd5b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afd5b-107">DESCRIPTION</span></span>
<span data-ttu-id="afd5b-108">Il cmdlet Set-AzureRmAnalysisServicesServer modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="afd5b-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="afd5b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afd5b-109">EXAMPLES</span></span>

### <span data-ttu-id="afd5b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afd5b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="afd5b-111">Modifica il server denominato TestServer in ResourceGroup TestGroup per impostare i tag come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="afd5b-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="afd5b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afd5b-112">PARAMETERS</span></span>

### <span data-ttu-id="afd5b-113">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="afd5b-113">-Administrator</span></span>
<span data-ttu-id="afd5b-114">Stringa che rappresenta un elenco delimitato da virgole di utenti o gruppi da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="afd5b-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="afd5b-115">Gli utenti o i gruppi devono essere specificati come formato user@contoso.com UPN, ad esempio groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="afd5b-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="afd5b-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="afd5b-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="afd5b-117">URI del contenitore BLOB per il backup del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="afd5b-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd5b-118">-DefaultProfile</span></span>
<span data-ttu-id="afd5b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afd5b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="afd5b-120">-DisableBackup</span></span>
<span data-ttu-id="afd5b-121">Il passaggio per disabilitare il contenitore di BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="afd5b-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="afd5b-122">Per riattivare il contenitore di BLOB di backup, fornisci l'URI del contenitore BLOB di backup come-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="afd5b-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="afd5b-123">-Name</span></span>
<span data-ttu-id="afd5b-124">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="afd5b-124">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="afd5b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afd5b-125">-PassThru</span></span>
<span data-ttu-id="afd5b-126">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="afd5b-126">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd5b-127">-ResourceGroupName</span></span>
<span data-ttu-id="afd5b-128">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="afd5b-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="afd5b-129">-Sku</span></span>
<span data-ttu-id="afd5b-130">Nome dell'USK per il server.</span><span class="sxs-lookup"><span data-stu-id="afd5b-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="afd5b-131">I valori supportati sono 0',' s 1',' s 2',' s 4' per il livello standard; ' B1',' B2' per il livello di base è da 1' per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="afd5b-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="afd5b-132">-Tag</span></span>
<span data-ttu-id="afd5b-133">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="afd5b-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="afd5b-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="afd5b-135">Conteggio delle riproduzioni di sola lettura di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="afd5b-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-136">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="afd5b-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="afd5b-137">Modalità di connessione predefinita di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="afd5b-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="afd5b-138">-FirewallConfig</span></span>
<span data-ttu-id="afd5b-139">Configurazione del firewall di un server di analisi</span><span class="sxs-lookup"><span data-stu-id="afd5b-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="afd5b-140">-Confirm</span></span>
<span data-ttu-id="afd5b-141">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="afd5b-141">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd5b-142">-WhatIf</span></span>
<span data-ttu-id="afd5b-143">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="afd5b-143">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd5b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd5b-144">CommonParameters</span></span>
<span data-ttu-id="afd5b-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd5b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd5b-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd5b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd5b-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afd5b-147">INPUTS</span></span>

### <span data-ttu-id="afd5b-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="afd5b-148">None</span></span>
<span data-ttu-id="afd5b-149">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="afd5b-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="afd5b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afd5b-150">OUTPUTS</span></span>

### <span data-ttu-id="afd5b-151">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="afd5b-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="afd5b-152">Note</span><span class="sxs-lookup"><span data-stu-id="afd5b-152">NOTES</span></span>
<span data-ttu-id="afd5b-153">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="afd5b-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="afd5b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afd5b-154">RELATED LINKS</span></span>

[<span data-ttu-id="afd5b-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="afd5b-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="afd5b-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="afd5b-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
