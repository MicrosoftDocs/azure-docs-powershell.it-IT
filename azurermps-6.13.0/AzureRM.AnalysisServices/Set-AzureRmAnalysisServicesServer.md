---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 30f5e7237f497f3d9f4208548b56ede72583f067
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686978"
---
# <span data-ttu-id="dabb1-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dabb1-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="dabb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dabb1-102">SYNOPSIS</span></span>
<span data-ttu-id="dabb1-103">Modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="dabb1-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dabb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dabb1-104">SYNTAX</span></span>

### <span data-ttu-id="dabb1-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dabb1-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabb1-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="dabb1-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dabb1-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="dabb1-107">DisassociateGateway</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dabb1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dabb1-108">DESCRIPTION</span></span>
<span data-ttu-id="dabb1-109">Il cmdlet Set-AzureRmAnalysisServicesServer modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="dabb1-109">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="dabb1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dabb1-110">EXAMPLES</span></span>

### <span data-ttu-id="dabb1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dabb1-111">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="dabb1-112">Modifica il server denominato TestServer in ResourceGroup TestGroup per impostare i tag come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="dabb1-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="dabb1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dabb1-113">PARAMETERS</span></span>

### <span data-ttu-id="dabb1-114">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="dabb1-114">-Administrator</span></span>
<span data-ttu-id="dabb1-115">Stringa che rappresenta un elenco delimitato da virgole di utenti o gruppi da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="dabb1-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="dabb1-116">Gli utenti o i gruppi devono essere specificati come formato user@contoso.com UPN, ad esempio groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="dabb1-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="dabb1-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="dabb1-118">URI del contenitore BLOB per il backup del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="dabb1-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="dabb1-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="dabb1-120">Modalità di connessione predefinita di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="dabb1-120">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabb1-121">-DefaultProfile</span></span>
<span data-ttu-id="dabb1-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dabb1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabb1-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="dabb1-123">-DisableBackup</span></span>
<span data-ttu-id="dabb1-124">Il passaggio per disabilitare il contenitore di BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="dabb1-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="dabb1-125">Per riattivare il contenitore di BLOB di backup, fornisci l'URI del contenitore BLOB di backup come-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="dabb1-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="dabb1-126">-DisassociateGateway</span></span>
<span data-ttu-id="dabb1-127">Dissocia risorsa gateway da un server di analisi</span><span class="sxs-lookup"><span data-stu-id="dabb1-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="dabb1-128">-FirewallConfig</span></span>
<span data-ttu-id="dabb1-129">Configurazione del firewall di un server di analisi</span><span class="sxs-lookup"><span data-stu-id="dabb1-129">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-130">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="dabb1-130">-GatewayResourceId</span></span>
<span data-ttu-id="dabb1-131">ID risorsa gateway per assocaite in un server di analisi</span><span class="sxs-lookup"><span data-stu-id="dabb1-131">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="dabb1-132">-Name</span></span>
<span data-ttu-id="dabb1-133">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="dabb1-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="dabb1-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dabb1-134">-PassThru</span></span>
<span data-ttu-id="dabb1-135">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="dabb1-135">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="dabb1-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="dabb1-137">Conteggio delle riproduzioni di sola lettura di un server di Analysis Service</span><span class="sxs-lookup"><span data-stu-id="dabb1-137">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabb1-138">-ResourceGroupName</span></span>
<span data-ttu-id="dabb1-139">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="dabb1-139">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="dabb1-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="dabb1-140">-Sku</span></span>
<span data-ttu-id="dabb1-141">Nome dell'USK per il server.</span><span class="sxs-lookup"><span data-stu-id="dabb1-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="dabb1-142">I valori supportati sono 0',' s 1',' s 2',' s 4' per il livello standard; ' B1',' B2' per il livello di base è da 1' per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="dabb1-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="dabb1-143">-Tag</span></span>
<span data-ttu-id="dabb1-144">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="dabb1-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dabb1-145">-Confirm</span></span>
<span data-ttu-id="dabb1-146">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="dabb1-146">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabb1-147">-WhatIf</span></span>
<span data-ttu-id="dabb1-148">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="dabb1-148">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabb1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabb1-149">CommonParameters</span></span>
<span data-ttu-id="dabb1-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabb1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabb1-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabb1-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabb1-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dabb1-152">INPUTS</span></span>

### <span data-ttu-id="dabb1-153">System. String</span><span class="sxs-lookup"><span data-stu-id="dabb1-153">System.String</span></span>

### <span data-ttu-id="dabb1-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dabb1-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dabb1-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dabb1-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dabb1-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dabb1-156">System.Int32</span></span>

### <span data-ttu-id="dabb1-157">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="dabb1-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="dabb1-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dabb1-158">OUTPUTS</span></span>

### <span data-ttu-id="dabb1-159">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dabb1-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="dabb1-160">Note</span><span class="sxs-lookup"><span data-stu-id="dabb1-160">NOTES</span></span>
<span data-ttu-id="dabb1-161">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="dabb1-161">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="dabb1-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dabb1-162">RELATED LINKS</span></span>

[<span data-ttu-id="dabb1-163">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dabb1-163">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="dabb1-164">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="dabb1-164">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
