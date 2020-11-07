---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685695"
---
# <span data-ttu-id="7ed8d-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7ed8d-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="7ed8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ed8d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed8d-103">Ottiene i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ed8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ed8d-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed8d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ed8d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed8d-106">Il cmdlet **Get-AzureRmBackupContainer** ottiene i contenitori di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="7ed8d-107">Un **AzureBackupContainer** incapsula origini dati, elementi protetti e punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="7ed8d-108">Un **AzureBackupContainer** può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ed8d-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="7ed8d-109">Un computer Windows Server</span><span class="sxs-lookup"><span data-stu-id="7ed8d-109">A Windows Server computer</span></span>
- <span data-ttu-id="7ed8d-110">Un server SCDPM (System Center Data Protection Manager)</span><span class="sxs-lookup"><span data-stu-id="7ed8d-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="7ed8d-111">Macchina virtuale di una infrastruttura Azure come servizio (IaaS)</span><span class="sxs-lookup"><span data-stu-id="7ed8d-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="7ed8d-112">Prima di poter eseguire il backup di un'origine dati o di un elemento, è necessario registrare il contenitore che lo contiene con il servizio di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="7ed8d-113">Il contenitore deve essere autenticato per inviare dati di backup al Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="7ed8d-114">Per i computer Windows Server e i server SCDPM, la registrazione viene mantenuta con il nome di dominio completo del server.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="7ed8d-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ed8d-115">EXAMPLES</span></span>

### <span data-ttu-id="7ed8d-116">Esempio 1: visualizzare tutti i server registrati in un Vault</span><span class="sxs-lookup"><span data-stu-id="7ed8d-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="7ed8d-117">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="7ed8d-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="7ed8d-118">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="7ed8d-119">Il secondo comando consente di ottenere tutti i contenitori di tipo Windows dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="7ed8d-120">Esempio 2: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="7ed8d-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="7ed8d-121">Questo comando ottiene il contenitore denominato DPMSERVER. CONTOSO.COM.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="7ed8d-122">Il comando specifica il Vault in $Vault e il tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="7ed8d-123">Esempio 3: visualizzare tutte le macchine virtuali di Azure registrate</span><span class="sxs-lookup"><span data-stu-id="7ed8d-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="7ed8d-124">Questo comando consente di ottenere le macchine virtuali registrate dal Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="7ed8d-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ed8d-125">PARAMETERS</span></span>

### <span data-ttu-id="7ed8d-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed8d-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="7ed8d-127">Specifica il nome del gruppo di risorse associato al contenitore.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-127">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="7ed8d-128">Questo nome è lo stesso valore specificato per il parametro *ServiceName* o *ResourceGroupName* del cmdlet Register-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-128">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="7ed8d-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ed8d-129">-Name</span></span>
<span data-ttu-id="7ed8d-130">Specifica il nome del contenitore ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-130">Specifies the name of the container that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ed8d-131">-Stato</span><span class="sxs-lookup"><span data-stu-id="7ed8d-131">-Status</span></span>
<span data-ttu-id="7ed8d-132">Specifica lo stato corrente dei contenitori ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-132">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="7ed8d-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ed8d-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7ed8d-134">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="7ed8d-134">NotRegistered</span></span> 
- <span data-ttu-id="7ed8d-135">Registrato</span><span class="sxs-lookup"><span data-stu-id="7ed8d-135">Registered</span></span> 
- <span data-ttu-id="7ed8d-136">Registrazione</span><span class="sxs-lookup"><span data-stu-id="7ed8d-136">Registering</span></span>

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

### <span data-ttu-id="7ed8d-137">-Digitare</span><span class="sxs-lookup"><span data-stu-id="7ed8d-137">-Type</span></span>
<span data-ttu-id="7ed8d-138">Specifica il tipo di contenitori ottenuti da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-138">Specifies the type of containers that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ed8d-139">-Vault</span><span class="sxs-lookup"><span data-stu-id="7ed8d-139">-Vault</span></span>
<span data-ttu-id="7ed8d-140">Specifica un archivio di backup da cui questo cmdlet ottiene i contenitori.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-140">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="7ed8d-141">Per ottenere un **AzureRmBackupVault** , usare il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-141">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="7ed8d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed8d-142">-DefaultProfile</span></span>
<span data-ttu-id="7ed8d-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ed8d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed8d-144">CommonParameters</span></span>
<span data-ttu-id="7ed8d-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed8d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed8d-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed8d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed8d-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ed8d-147">INPUTS</span></span>

### <span data-ttu-id="7ed8d-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="7ed8d-148">AzureBackupVault</span></span>

## <span data-ttu-id="7ed8d-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ed8d-149">OUTPUTS</span></span>

### <span data-ttu-id="7ed8d-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7ed8d-150">AzureBackupContainer</span></span>

## <span data-ttu-id="7ed8d-151">Note</span><span class="sxs-lookup"><span data-stu-id="7ed8d-151">NOTES</span></span>
* <span data-ttu-id="7ed8d-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7ed8d-152">None</span></span>

## <span data-ttu-id="7ed8d-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ed8d-153">RELATED LINKS</span></span>

[<span data-ttu-id="7ed8d-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7ed8d-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7ed8d-155">Registro-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7ed8d-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="7ed8d-156">Annullamento della registrazione-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="7ed8d-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)

