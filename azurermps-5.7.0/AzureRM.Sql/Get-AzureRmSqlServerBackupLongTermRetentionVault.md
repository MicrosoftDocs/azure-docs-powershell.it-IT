---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 686785F8-2085-4705-A74D-12B18A87E187
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 567cb47599a23bf83581afb97a425902ee0e159a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512239"
---
# <span data-ttu-id="b087f-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b087f-101">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="b087f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b087f-102">SYNOPSIS</span></span>
<span data-ttu-id="b087f-103">Ottiene un Vault di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="b087f-103">Gets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b087f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b087f-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerBackupLongTermRetentionVault [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b087f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b087f-105">DESCRIPTION</span></span>
<span data-ttu-id="b087f-106">Il cmdlet **Get-AzureRmSqlServerBackupLongTermRetentionVault** ottiene il Vault di conservazione a lungo termine registrato nel server.</span><span class="sxs-lookup"><span data-stu-id="b087f-106">The **Get-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet gets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="b087f-107">Il Vault è una risorsa di backup di Azure usata per archiviare i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="b087f-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="b087f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b087f-108">EXAMPLES</span></span>

## <span data-ttu-id="b087f-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b087f-109">PARAMETERS</span></span>

### <span data-ttu-id="b087f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b087f-110">-DefaultProfile</span></span>
<span data-ttu-id="b087f-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b087f-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b087f-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b087f-112">-ResourceGroupName</span></span>
<span data-ttu-id="b087f-113">Specifica il nome del gruppo di risorse che contiene il server.</span><span class="sxs-lookup"><span data-stu-id="b087f-113">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="b087f-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b087f-114">-ServerName</span></span>
<span data-ttu-id="b087f-115">Specifica il server per cui questo cmdlet ottiene un Vault.</span><span class="sxs-lookup"><span data-stu-id="b087f-115">Specifies the server for which this cmdlet gets a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b087f-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b087f-116">-Confirm</span></span>
<span data-ttu-id="b087f-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b087f-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b087f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b087f-118">-WhatIf</span></span>
<span data-ttu-id="b087f-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b087f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b087f-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b087f-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b087f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b087f-121">CommonParameters</span></span>
<span data-ttu-id="b087f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b087f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b087f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b087f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b087f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b087f-124">INPUTS</span></span>

### <span data-ttu-id="b087f-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b087f-125">None</span></span>
<span data-ttu-id="b087f-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b087f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b087f-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b087f-127">OUTPUTS</span></span>

## <span data-ttu-id="b087f-128">Note</span><span class="sxs-lookup"><span data-stu-id="b087f-128">NOTES</span></span>

## <span data-ttu-id="b087f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b087f-129">RELATED LINKS</span></span>

[<span data-ttu-id="b087f-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="b087f-130">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Set-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="b087f-131">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b087f-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
