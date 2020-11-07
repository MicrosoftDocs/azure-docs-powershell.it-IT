---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685954"
---
# <span data-ttu-id="4dded-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4dded-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="4dded-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dded-102">SYNOPSIS</span></span>
<span data-ttu-id="4dded-103">Ottiene i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="4dded-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dded-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dded-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dded-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dded-105">DESCRIPTION</span></span>
<span data-ttu-id="4dded-106">Il cmdlet **Get-AzureRmBackupContainer** ottiene i contenitori di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="4dded-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>
<span data-ttu-id="4dded-107">Un **AzureBackupContainer** incapsula origini dati, elementi protetti e punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4dded-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="4dded-108">Un **AzureBackupContainer** può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="4dded-108">An **AzureBackupContainer** can be one of the following:</span></span> 
- <span data-ttu-id="4dded-109">Un computer Windows Server</span><span class="sxs-lookup"><span data-stu-id="4dded-109">A Windows Server computer</span></span>
- <span data-ttu-id="4dded-110">Un server SCDPM (System Center Data Protection Manager)</span><span class="sxs-lookup"><span data-stu-id="4dded-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="4dded-111">Una macchina virtuale dell'infrastruttura Azure come servizio (IaaS) prima del backup può eseguire il backup di un'origine dati o di un elemento, è necessario registrare il contenitore che lo contiene con il servizio di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="4dded-111">An Azure infrastructure as a service (IaaS) virtual machine Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="4dded-112">Il contenitore deve essere autenticato per inviare dati di backup al Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="4dded-112">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="4dded-113">Per i computer Windows Server e i server SCDPM, la registrazione viene mantenuta con il nome di dominio completo del server.</span><span class="sxs-lookup"><span data-stu-id="4dded-113">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="4dded-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dded-114">EXAMPLES</span></span>

### <span data-ttu-id="4dded-115">Esempio 1: visualizzare tutti i server registrati in un Vault</span><span class="sxs-lookup"><span data-stu-id="4dded-115">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="4dded-116">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="4dded-116">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="4dded-117">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="4dded-117">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="4dded-118">Il secondo comando consente di ottenere tutti i contenitori di tipo Windows dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="4dded-118">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="4dded-119">Esempio 2: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="4dded-119">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="4dded-120">Questo comando ottiene il contenitore denominato DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="4dded-120">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="4dded-121">Il comando specifica il Vault in $Vault e il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="4dded-121">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="4dded-122">Esempio 3: visualizzare tutte le macchine virtuali di Azure registrate</span><span class="sxs-lookup"><span data-stu-id="4dded-122">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="4dded-123">Questo comando consente di ottenere le macchine virtuali registrate dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="4dded-123">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="4dded-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dded-124">PARAMETERS</span></span>

### <span data-ttu-id="4dded-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dded-125">-DefaultProfile</span></span>
<span data-ttu-id="4dded-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4dded-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dded-127">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dded-127">-ManagedResourceGroupName</span></span>
<span data-ttu-id="4dded-128">Specifica il nome del gruppo di risorse associato al contenitore.</span><span class="sxs-lookup"><span data-stu-id="4dded-128">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="4dded-129">Questo nome è lo stesso valore specificato per il parametro *ServiceName* o *ResourceGroupName* del cmdlet Register-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="4dded-129">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dded-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dded-130">-Name</span></span>
<span data-ttu-id="4dded-131">Specifica il nome del contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dded-131">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dded-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="4dded-132">-Status</span></span>
<span data-ttu-id="4dded-133">Specifica lo stato corrente dei contenitori ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dded-133">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="4dded-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4dded-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4dded-135">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="4dded-135">NotRegistered</span></span> 
- <span data-ttu-id="4dded-136">Registrato</span><span class="sxs-lookup"><span data-stu-id="4dded-136">Registered</span></span> 
- <span data-ttu-id="4dded-137">Registrazione</span><span class="sxs-lookup"><span data-stu-id="4dded-137">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dded-138">-Digitare</span><span class="sxs-lookup"><span data-stu-id="4dded-138">-Type</span></span>
<span data-ttu-id="4dded-139">Specifica il tipo di contenitori ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dded-139">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dded-140">-Vault</span><span class="sxs-lookup"><span data-stu-id="4dded-140">-Vault</span></span>
<span data-ttu-id="4dded-141">Specifica un archivio di backup da cui questo cmdlet ottiene i contenitori.</span><span class="sxs-lookup"><span data-stu-id="4dded-141">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="4dded-142">Per ottenere un **AzureRmBackupVault** , usare il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="4dded-142">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dded-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dded-143">CommonParameters</span></span>
<span data-ttu-id="4dded-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dded-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dded-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dded-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dded-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dded-146">INPUTS</span></span>

### <span data-ttu-id="4dded-147">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dded-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="4dded-148">Parameters: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4dded-148">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="4dded-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dded-149">OUTPUTS</span></span>

### <span data-ttu-id="4dded-150">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4dded-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>

## <span data-ttu-id="4dded-151">Note</span><span class="sxs-lookup"><span data-stu-id="4dded-151">NOTES</span></span>
* <span data-ttu-id="4dded-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4dded-152">None</span></span>

## <span data-ttu-id="4dded-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dded-153">RELATED LINKS</span></span>

[<span data-ttu-id="4dded-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4dded-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="4dded-155">Registro-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4dded-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="4dded-156">Annullamento della registrazione-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4dded-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


