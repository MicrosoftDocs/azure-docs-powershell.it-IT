---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508867"
---
# <span data-ttu-id="0f341-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0f341-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="0f341-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f341-102">SYNOPSIS</span></span>
<span data-ttu-id="0f341-103">Modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="0f341-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f341-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f341-104">SYNTAX</span></span>

### <span data-ttu-id="0f341-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f341-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f341-106">Disabilitare il backup</span><span class="sxs-lookup"><span data-stu-id="0f341-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f341-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f341-107">DESCRIPTION</span></span>
<span data-ttu-id="0f341-108">Il cmdlet Set-AzureRmAnalysisServicesServer modifica un'istanza di Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="0f341-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="0f341-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f341-109">EXAMPLES</span></span>

### <span data-ttu-id="0f341-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f341-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="0f341-111">Modifica il server denominato TestServer in ResourceGroup TestGroup per impostare i tag come Key1: value1 e key2: value2 e administrator to testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0f341-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="0f341-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f341-112">PARAMETERS</span></span>

### <span data-ttu-id="0f341-113">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="0f341-113">-Administrator</span></span>
<span data-ttu-id="0f341-114">Stringa che rappresenta un elenco delimitato da virgole di utenti o gruppi da impostare come amministratori nel server.</span><span class="sxs-lookup"><span data-stu-id="0f341-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="0f341-115">Gli utenti o i gruppi devono essere specificati come formato user@contoso.com UPN, ad esempio groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="0f341-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="0f341-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0f341-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="0f341-117">URI del contenitore BLOB per il backup del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0f341-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="0f341-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="0f341-118">-DisableBackup</span></span>
<span data-ttu-id="0f341-119">Il passaggio per disabilitare il contenitore di BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="0f341-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="0f341-120">Per riattivare il contenitore di BLOB di backup, fornisci l'URI del contenitore BLOB di backup come-BackupBlobContainerUri.</span><span class="sxs-lookup"><span data-stu-id="0f341-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f341-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f341-121">-Name</span></span>
<span data-ttu-id="0f341-122">Nome del server di Analysis Services</span><span class="sxs-lookup"><span data-stu-id="0f341-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="0f341-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f341-123">-PassThru</span></span>
<span data-ttu-id="0f341-124">Restituirà i dettagli del server eliminati se l'operazione viene completata correttamente</span><span class="sxs-lookup"><span data-stu-id="0f341-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="0f341-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f341-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f341-126">Nome del gruppo di risorse Azure a cui appartiene il server</span><span class="sxs-lookup"><span data-stu-id="0f341-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="0f341-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="0f341-127">-Sku</span></span>
<span data-ttu-id="0f341-128">Nome dell'USK per il server.</span><span class="sxs-lookup"><span data-stu-id="0f341-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="0f341-129">I valori supportati sono 0',' s 1',' s 2',' s 4' per il livello standard; ' B1',' B2' per il livello di base è da 1' per il livello di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="0f341-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="0f341-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f341-130">-Tag</span></span>
<span data-ttu-id="0f341-131">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="0f341-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="0f341-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f341-132">-Confirm</span></span>
<span data-ttu-id="0f341-133">Chiede all'utente di confermare se eseguire l'operazione</span><span class="sxs-lookup"><span data-stu-id="0f341-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="0f341-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f341-134">-WhatIf</span></span>
<span data-ttu-id="0f341-135">Descrive le azioni che verranno eseguite dall'operazione corrente senza eseguirle effettivamente</span><span class="sxs-lookup"><span data-stu-id="0f341-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="0f341-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f341-136">-DefaultProfile</span></span>
<span data-ttu-id="0f341-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f341-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f341-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f341-138">CommonParameters</span></span>
<span data-ttu-id="0f341-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f341-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f341-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f341-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f341-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f341-141">INPUTS</span></span>

## <span data-ttu-id="0f341-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f341-142">OUTPUTS</span></span>

### <span data-ttu-id="0f341-143">Microsoft. Azure. Management. Analysis. Models. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0f341-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="0f341-144">Note</span><span class="sxs-lookup"><span data-stu-id="0f341-144">NOTES</span></span>
<span data-ttu-id="0f341-145">Alias: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="0f341-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="0f341-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f341-146">RELATED LINKS</span></span>

[<span data-ttu-id="0f341-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0f341-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="0f341-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0f341-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
