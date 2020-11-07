---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519913"
---
# <span data-ttu-id="b700a-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b700a-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="b700a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b700a-102">SYNOPSIS</span></span>
<span data-ttu-id="b700a-103">Registra il contenitore con un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="b700a-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b700a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b700a-104">SYNTAX</span></span>

### <span data-ttu-id="b700a-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="b700a-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b700a-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="b700a-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b700a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b700a-107">DESCRIPTION</span></span>
<span data-ttu-id="b700a-108">Il cmdlet **Register-AzureRmBackupContainer** registra il contenitore con un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="b700a-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="b700a-109">Per configurare il backup con Azure Backup, prima di tutto registrare il server o la macchina virtuale con un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="b700a-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="b700a-110">Questo cmdlet registra una macchina virtuale dell'infrastruttura come servizio (IaaS) con il Vault specificato.</span><span class="sxs-lookup"><span data-stu-id="b700a-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="b700a-111">L'operazione Register associa la macchina virtuale Azure alla volta di backup e tiene traccia della macchina virtuale tramite il ciclo di vita del backup.</span><span class="sxs-lookup"><span data-stu-id="b700a-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="b700a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b700a-112">EXAMPLES</span></span>

### <span data-ttu-id="b700a-113">Esempio 1: registrare una macchina virtuale in un caveau di backup</span><span class="sxs-lookup"><span data-stu-id="b700a-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="b700a-114">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="b700a-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="b700a-115">Il comando Archivia il Vault nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="b700a-115">The command stores the vault in the $Vault variable.</span></span>

<span data-ttu-id="b700a-116">Il secondo comando registra la macchina virtuale denominata Contoso03Vm con il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="b700a-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="b700a-117">La macchina virtuale appartiene al servizio denominato ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="b700a-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="b700a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b700a-118">PARAMETERS</span></span>

### <span data-ttu-id="b700a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b700a-119">-DefaultProfile</span></span>
<span data-ttu-id="b700a-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b700a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b700a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b700a-121">-Name</span></span>
<span data-ttu-id="b700a-122">Specifica il nome della macchina virtuale registrata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b700a-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b700a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b700a-123">-ResourceGroupName</span></span>
<span data-ttu-id="b700a-124">Specifica il nome del gruppo di risorse per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b700a-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b700a-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b700a-125">-ServiceName</span></span>
<span data-ttu-id="b700a-126">Specifica il nome del servizio della macchina virtuale che questo cmdlet registra.</span><span class="sxs-lookup"><span data-stu-id="b700a-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>

<span data-ttu-id="b700a-127">In genere, il nome di un servizio cloud ha un suffisso. cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="b700a-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="b700a-128">Non includere il suffisso quando specifichi questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b700a-128">Do not include the suffix when you specify this parameter.</span></span>

<span data-ttu-id="b700a-129">Per ottenere informazioni su una macchina virtuale, usare il cmdlet Get-AzureRMVM.</span><span class="sxs-lookup"><span data-stu-id="b700a-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="b700a-130">Il nome del servizio è la proprietà **DeploymentName** dell'oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b700a-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b700a-131">-Vault</span><span class="sxs-lookup"><span data-stu-id="b700a-131">-Vault</span></span>
<span data-ttu-id="b700a-132">Specifica il Vault di backup a cui questo cmdlet registra la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b700a-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="b700a-133">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="b700a-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b700a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b700a-134">CommonParameters</span></span>
<span data-ttu-id="b700a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b700a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b700a-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b700a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b700a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b700a-137">INPUTS</span></span>

### <span data-ttu-id="b700a-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b700a-138">AzureRmBackupVault</span></span>

## <span data-ttu-id="b700a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b700a-139">OUTPUTS</span></span>

### <span data-ttu-id="b700a-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b700a-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="b700a-141">Note</span><span class="sxs-lookup"><span data-stu-id="b700a-141">NOTES</span></span>

## <span data-ttu-id="b700a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b700a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b700a-143">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b700a-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

