---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519922"
---
# <span data-ttu-id="b2244-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="b2244-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="b2244-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2244-102">SYNOPSIS</span></span>
<span data-ttu-id="b2244-103">Registra nuovamente un server per la connessione a un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="b2244-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2244-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2244-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2244-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2244-105">DESCRIPTION</span></span>
<span data-ttu-id="b2244-106">Il cmdlet **Enable-AzureRmBackupContainerReregistration** registra nuovamente un server per la connessione a un Vault di backup di Azure e continua la catena del punto di ripristino del backup.</span><span class="sxs-lookup"><span data-stu-id="b2244-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="b2244-107">Se si distrugge un server, tutti i punti di backup del cloud rimarranno nell'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="b2244-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="b2244-108">Se si crea un server sostitutivo e lo si assegna allo stesso nome di dominio completo, è possibile riconnettere il server allo stesso Vault.</span><span class="sxs-lookup"><span data-stu-id="b2244-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="b2244-109">Questo cmdlet consente di eseguire il backup per creare backup e aggiungere nuovi punti di backup al set esistente.</span><span class="sxs-lookup"><span data-stu-id="b2244-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="b2244-110">Il nuovo server continua nella catena di backup.</span><span class="sxs-lookup"><span data-stu-id="b2244-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="b2244-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2244-111">EXAMPLES</span></span>

## <span data-ttu-id="b2244-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2244-112">PARAMETERS</span></span>

### <span data-ttu-id="b2244-113">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="b2244-113">-Container</span></span>
<span data-ttu-id="b2244-114">Specifica il contenitore di cui questo cmdlet viene riregistrato.</span><span class="sxs-lookup"><span data-stu-id="b2244-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="b2244-115">Per ottenere un **AzureRmBackupContainer** , usare il cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="b2244-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2244-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2244-116">-DefaultProfile</span></span>
<span data-ttu-id="b2244-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b2244-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2244-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2244-118">CommonParameters</span></span>
<span data-ttu-id="b2244-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2244-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2244-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2244-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2244-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2244-121">INPUTS</span></span>

### <span data-ttu-id="b2244-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b2244-122">AzureBackupContainer</span></span>

## <span data-ttu-id="b2244-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2244-123">OUTPUTS</span></span>

### <span data-ttu-id="b2244-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b2244-124">None</span></span>

## <span data-ttu-id="b2244-125">Note</span><span class="sxs-lookup"><span data-stu-id="b2244-125">NOTES</span></span>

## <span data-ttu-id="b2244-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2244-126">RELATED LINKS</span></span>

[<span data-ttu-id="b2244-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b2244-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b2244-128">Registro-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b2244-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


