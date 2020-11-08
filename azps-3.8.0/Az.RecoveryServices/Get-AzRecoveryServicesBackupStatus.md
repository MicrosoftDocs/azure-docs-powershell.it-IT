---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 1e10fe2aa534e236c99468ec672e6a0eeadae469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022677"
---
# <span data-ttu-id="150a5-101">Get-AzRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="150a5-101">Get-AzRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="150a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="150a5-102">SYNOPSIS</span></span>
<span data-ttu-id="150a5-103">Verifica se è stato eseguito il backup della risorsa ARM o meno.</span><span class="sxs-lookup"><span data-stu-id="150a5-103">Checks whether your ARM resource is backed up or not.</span></span>

## <span data-ttu-id="150a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="150a5-104">SYNTAX</span></span>

### <span data-ttu-id="150a5-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="150a5-105">Name (Default)</span></span>
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="150a5-106">IdWorkload</span><span class="sxs-lookup"><span data-stu-id="150a5-106">IdWorkload</span></span>
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="150a5-107">ID</span><span class="sxs-lookup"><span data-stu-id="150a5-107">Id</span></span>
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="150a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="150a5-108">DESCRIPTION</span></span>
<span data-ttu-id="150a5-109">Il comando restituisce null/Empty se la risorsa specificata non è protetta in un Vault di servizi di recupero nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="150a5-109">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="150a5-110">Se è protetta, verranno restituiti i dettagli relativi alla volta.</span><span class="sxs-lookup"><span data-stu-id="150a5-110">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="150a5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="150a5-111">EXAMPLES</span></span>

### <span data-ttu-id="150a5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="150a5-112">Example 1</span></span>
```
PS C:\> $status = Get-AzRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="150a5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="150a5-113">PARAMETERS</span></span>

### <span data-ttu-id="150a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150a5-114">-DefaultProfile</span></span>
<span data-ttu-id="150a5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="150a5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150a5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="150a5-116">-Name</span></span>
<span data-ttu-id="150a5-117">Nome della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da un Vault di servizi di ripristino nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="150a5-117">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150a5-118">-ProtectableObjectName</span><span class="sxs-lookup"><span data-stu-id="150a5-118">-ProtectableObjectName</span></span>
<span data-ttu-id="150a5-119">Nome della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da un Vault di servizi di ripristino nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="150a5-119">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="150a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="150a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="150a5-121">Nome del gruppo di risorse della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da qualche volta di RecoveryServices nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="150a5-121">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150a5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="150a5-122">-ResourceId</span></span>
<span data-ttu-id="150a5-123">ID della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da qualche volta di RecoveryServices nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="150a5-123">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="150a5-124">-Digitare</span><span class="sxs-lookup"><span data-stu-id="150a5-124">-Type</span></span>
<span data-ttu-id="150a5-125">Nome della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da un Vault di servizi di ripristino nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="150a5-125">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="150a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150a5-126">CommonParameters</span></span>
<span data-ttu-id="150a5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150a5-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="150a5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150a5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="150a5-129">INPUTS</span></span>

### <span data-ttu-id="150a5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="150a5-130">System.String</span></span>

## <span data-ttu-id="150a5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="150a5-131">OUTPUTS</span></span>

### <span data-ttu-id="150a5-132">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="150a5-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="150a5-133">Note</span><span class="sxs-lookup"><span data-stu-id="150a5-133">NOTES</span></span>

## <span data-ttu-id="150a5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="150a5-134">RELATED LINKS</span></span>
